# `Edgehog.Containers.Deployment.Starter`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/deployment/starter.ex#L21)

Deployments starter.

This server can be started when a device goes online. It will load all the
pending deployments of such device and start them trough the `Supervisor`.

# `child_spec`

Returns a specification to start this module under a supervisor.

See `Supervisor`.

# `cook`

Registers a new starter under the appropriate supervisor.

Given a device creates the appropriate child spec and sends it to the
Edgehog.Containers.Deployment.Starter.Supervisor supervisor.

The process will registry to the appropriate registry according to the
`name/1` function. See `start_link/1` docs for more.

# `name`

# `start_link`

Starts a new starter. The service will register to the appropriate registry
using the `:via` tuple.

The args must contain a `:device` and a `:tenant` keyword, respectively with
the device and tenant the operation will be performed for.

