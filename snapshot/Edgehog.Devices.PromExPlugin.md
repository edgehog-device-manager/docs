# `Edgehog.Devices.PromExPlugin`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/devices/prom_ex_plugin.ex#L21)

PromEx plugin for tenant fleet metrics.

Device metrics are driven by the telemetry events emitted when a device is
created, destroyed, connects or disconnects, so that no change is missed
between two polls. Forwarder sessions are stored only on Astarte, so they are
counted from the events emitted when they are requested and when the device
reports them as connected.

