# `Edgehog.Containers.Provisioner.Behaviour`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/provisioner/behaviour.ex#L21)

Behaviour describing the API of a Provisioner for a resource.

A Provisioner is a `GenServer` that takes a resource to provision on a
device, and orchestrates the whole provisioning flow with the device:
sending requests, managing timeouts, retries and errors, reacting to the
events emitted by the device, and broadcasting readiness (or failure).

This module shouldn't be used directly. Rather, it's best to
use `Edgehog.Containers.Provisioner`, i.e.:

```ex
defmodule ResourceProvisioner do
  use Edgehog.Containers.Provisioner, resource: ResourceModule
end
```

which will add the default implementation of a `Provisioner`.
All of the functions of this behaviour are overridable.
Note that a `Provisioner` is a `GenServer`, so you can also override any of
its callbacks, if you need.

# `provision_opts`

```elixir
@type provision_opts() :: start_opts() | keyword()
```

# `resource`

```elixir
@type resource() :: Ash.Resource.record()
```

An `Ash.Resource.record()` representing the resource to provision on a device.

# `start_opts`

```elixir
@type start_opts() :: [
  resource: resource(),
  tenant: Edgehog.Tenants.Tenant.t() | pos_integer(),
  mode: :auto | :manual
]
```

# `state`

```elixir
@type state() :: %{
  resource: resource(),
  tenant: Edgehog.Tenants.Tenant.t(),
  state: :init | :sent,
  retries: non_neg_integer()
}
```

The state map of the provisioner.

In the default implementation, it includes other key on top of the required ones:
%{
  device_online?: boolean(),
  mode: :auto | :manual
}

# `provision`

```elixir
@callback provision(
  resource(),
  Edgehog.Tenants.Tenant.t() | pos_integer(),
  provision_opts()
) :: GenServer.on_start()
```

Starts the right process through the correct (usually dynamic) supervisor.

This callback is optional: the default implementation starts the provisioner
under the supervisor specified by the `@sup` module attribute of the module
using `Edgehog.Containers.Provisioner`, so the user of the macro decides
where the process is spawned. When creating the link, the server checks a
registry to know whether the corresponding process is already up and running.
Check `Core.name/1` docs for more info.

# `start`

```elixir
@callback start(start_opts()) :: GenServer.on_start()
```

Starts a provisioner for a resource, without linking it to the
current process.

See `start_link/1` docs for more information.

# `start_link`

```elixir
@callback start_link(start_opts()) :: GenServer.on_start()
```

Starts a provisioner for a resource, linking the current process to
the provisioner one.

The default implementation for a provisioner of a resource follows the
following flow:

- checks that the resource is not ready already (i.e., the device never received it).
- tries to send the deployment information to astarte (calling `Core.send_to_device/2`).
- if an unrecoverable error occurs, broadcasts a failure on the `Core.topic/1` topic.
- if successful, waits for events on the resource itself.

- if a trigger reaches edgehog, it changes a property in the resource, emitting an event for the provisioner.
- the provisioner understands that the resource is ready, so it exits successfully.

- if no messages are incoming after a timer defined through the `timeout/1` function:
  + checks for readiness of the resource, maybe we just missed the message
  + queries astarte, maybe the trigger was missing
  + retries to send the message to the device.
  + loops with a new timeout set by the `timeout/1` function.

# `timeout`

```elixir
@callback timeout(state()) :: timeout()
```

Returns the timeout for retries.

In the default implementation, it is an exponential backoff timeout:
it reads information from the provisioner state (current send state, and
number of retries that happened), and it computes the timeout with the
following formula

```
timeout = pad + (2^retries) + rand(0,1000)
timeout = min(timeout, max_timeout)
```

- pad       :: the pad component is there to ensure a minimum timeout is
guaranteed. The pad is only applied when the resource
has been sent, and therefore we're waiting for astarte triggers
- 2^retries :: this is the exponential component, increases at each retry to
ensure we don't DDoS astarte/the device.
- rand      :: a random (between 0 and 1s) ensures no synchronization errors
appear.

