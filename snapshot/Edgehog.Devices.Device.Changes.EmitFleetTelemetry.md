# `Edgehog.Devices.Device.Changes.EmitFleetTelemetry`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/devices/device/changes/emit_fleet_telemetry.ex#L21)

Emits the fleet telemetry when a device is created or destroyed, or when its
`online` status changes.

The previous state is read before the write (locking the row) so that
upserts, which don't expose the old values, are tracked as well. Events are
emitted only once the transaction has been committed.

