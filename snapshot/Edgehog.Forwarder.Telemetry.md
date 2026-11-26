# `Edgehog.Forwarder.Telemetry`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/forwarder/telemetry.ex#L21)

Emits the telemetry events of the forwarder feature.

Events can be emitted on the following topics:

- `[:edgehog, :forwarder, :session, :requested]` when a new forwarder session
  is requested to a device. Metadata contains `tenant_slug`.
- `[:edgehog, :forwarder, :session, :connected]` when a device reports that
  it connected to a forwarder session. Metadata contains `tenant_slug`.

# `session_connected`

# `session_connected_event`

# `session_requested`

# `session_requested_event`

