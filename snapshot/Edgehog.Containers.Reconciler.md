# `Edgehog.Containers.Reconciler`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/containers/reconciler/reconciler.ex#L21)

Reconciler for container-related data between the device and the backend.

When a device connects a timeout gets set up: after a configurable amount of
time the reconciler goes trough all the data published by the device and
reconciles the state of the backend with the state of the astarte messages.

This is useful for a couple of reasons: the backend might have missed some
messages in trigger handling, the device might have not re-published some
property, not triggering a trigger and so on.

This process ensures that the state of the device is eventually consistent
with astarte state.

# `child_spec`

Returns a specification to start this module under a supervisor.

See `Supervisor`.

# `register_device`

# `start_link`

# `stop_device`

