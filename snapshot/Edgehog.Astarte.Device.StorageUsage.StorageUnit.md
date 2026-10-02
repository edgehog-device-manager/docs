# `Edgehog.Astarte.Device.StorageUsage.StorageUnit`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/astarte/device/storage_usage/storage_unit.ex#L21)

Device storage units. They represent a storage available on a device and
provide insightful data on it:

- label       :: is the storage identification label. Unique per storage unit.
- mounts      :: is a list of paths mounted on the device.
- name        :: an optional name for the storage
- fstype      :: the filesystem type of the storage unit
- kind        :: the storage unit kind
- total_bytes :: the storage unit total bytes
- free_bytes  :: the storage unit free bytes

# `t`

```elixir
@type t() :: %Edgehog.Astarte.Device.StorageUsage.StorageUnit{
  free_bytes: integer() | nil,
  fstype: String.t() | nil,
  kind: String.t() | nil,
  label: String.t(),
  mounts: [String.t()] | nil,
  name: String.t() | nil,
  total_bytes: integer() | nil
}
```

