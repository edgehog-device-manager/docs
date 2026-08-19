# `Edgehog.Containers.Container.Deployment.Provisioner`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/container/deployment/provisioner.ex#L21)

A container deployment provisioner.

Each and every time a container should be deployed, it can be done through this
provisioner. The provisioner sends the appropriate messages to the device and
emits a `container_deployments:provisioning:<id>` event whenever container is present in the
device.

The provisioning flow can be described as follows:

- `start_link/1` called, init the process
- The server subscribes to events on `container_deployments:<id>` (id of the container
  deployment)
- if the container deployment is already ready, the provisioner terminates
  normally right away, broadcasting readiness
- otherwise the appropriate messages are sent to the device through the
  `Core` module (see `Core.send/1` docs for more info)

Nice flow (everything goes ok)
- Astarte triggers update the container deployment state, marking it as present or
  not present and emitting an event on the correct topic
- The server reacts to the event, handles the message and emits an event on
  `container_deployments:provisioning:<id>` when the container is ready
- listening processes can react to this information

Timeouts (something goes wrong)
- `Core.send/1` failed, maybe the device is offline, or there was some
  problem with astarte
- an exponential backoff timeout is started
- A :timeout hits the server, it retries to send the container information to the
  device

For more information, check the `Edgehog.Containers.Provisioner` docs.

# `child_spec`

Returns a specification to start this module under a supervisor.

See `Supervisor`.

