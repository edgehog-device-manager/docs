# `Edgehog.Containers.Provisioner`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/provisioner.ex#L21)

This module provides the default implementation for `Edgehog.Containers.Provisioner.Behaviour`.
It is sufficient to add a using statement like so:

```ex
defmodule ResourceDeployment.Provisioner do
  @sup Edgehog.Containers.Resource.Provisioner.Supervisor

  use Edgehog.Containers.Provisioner, resource: Edgehog.Containers.Resource.Deployment, core: Core
end
```

where `resource` is the module of the resource to provision. The provisioner
is a `GenServer` that takes a resource (not just deployments) and orchestrates
the whole provisioning with the device: sending requests, managing timeouts,
retries and errors.

The resource specific logic is delegated to the `Core` module nested inside
the provisioner (see `Edgehog.Containers.Provisioner.Core.Behaviour`): pure
functions that can be tested in isolation (e.g. `ready?/1`, `topic/1`) and
functions that provide the side effects of the provisioning (e.g.
`send_to_device/2`, `reconcile/2`).

The provisioning flow can be described as follows:

- `start_link/1` called, initializing the process and subscribing to the
  events emitted on `Core.subscribe_topic/1`
- if the resource is already ready, the provisioner terminates normally
  right away, broadcasting readiness
- otherwise the appropriate messages are sent to the device through the
  `Core` module (see `Core.send_to_device/2` docs for more info)

Nice flow (everything goes ok)
- Astarte triggers update the resource state, marking it as present or
not present and emitting an event on the correct topic
- The server reacts to the event, handles the message and emits an event on
`Core.topic/1` when the resource is ready
- listening processes can react to this information

Timeouts (something goes wrong)
- `Core.send_to_device/2` failed, maybe the device is offline, or there was
  some problem with astarte
- an exponential backoff timeout is started
- A :timeout hits the server, it retries to send the resource information to
  the device

