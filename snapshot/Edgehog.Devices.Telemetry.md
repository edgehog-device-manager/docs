# `Edgehog.Devices.Telemetry`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/devices/telemetry.ex#L21)

Emits the telemetry events of the devices fleet.

Events can be emitted on the following topics:

- `[:edgehog, :devices, :total_changed]` when a device is created or
  destroyed. Measurements contain `delta` (`1` or `-1`). Metadata contains
  `tenant_slug`.
- `[:edgehog, :devices, :connected_changed]` when a device goes online or
  offline, including when an online device is destroyed. Measurements
  contain `delta` (`1` or `-1`). Metadata contains `tenant_slug`.

# `connected_changed_event`

# `device_connected`

# `device_created`

# `device_destroyed`

# `device_disconnected`

# `total_changed_event`

