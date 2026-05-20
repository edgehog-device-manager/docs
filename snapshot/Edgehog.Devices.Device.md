# `Edgehog.Devices.Device`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/devices/device/device.ex#L21)

Device resource schema and operations.

Denotes a device instance that connects and exchanges data.

Each Device is associated to a specific SystemModel, which in turn is
associated to a specific HardwareType.
A Device also exposes info about its connection status and some sets of data read by its operating system.

# `t`

```elixir
@type t() :: %Edgehog.Devices.Device{
  __lateral_join_source__: term(),
  __meta__: term(),
  __metadata__: term(),
  __order__: term(),
  aggregates: term(),
  appengine_client: term(),
  application_deployments: term(),
  application_releases: term(),
  available_containers: term(),
  available_deployments: term(),
  available_device_mappings: term(),
  available_images: term(),
  available_networks: term(),
  available_volumes: term(),
  base_image: term(),
  battery_status: term(),
  calculations: term(),
  capabilities: term(),
  cellular_connection: term(),
  container_deployments: term(),
  device_groups: term(),
  device_id: term(),
  device_mapping_deployments: term(),
  device_status: term(),
  file_delete_requests: term(),
  file_download_requests: term(),
  file_transfer_capabilities: term(),
  file_upload_requests: term(),
  forwarder_sessions: term(),
  hardware_info: term(),
  id: term(),
  image_deployments: term(),
  inserted_at: term(),
  last_connection: term(),
  last_disconnection: term(),
  last_seen_ip: term(),
  location: term(),
  modem_properties: term(),
  modem_status: term(),
  name: term(),
  network_deployments: term(),
  network_interfaces: term(),
  online: term(),
  os_info: term(),
  ota_operations: term(),
  part_number: term(),
  position: term(),
  realm: term(),
  realm_id: term(),
  runtime_info: term(),
  sensor_positions: term(),
  serial_number: term(),
  storage_usage: term(),
  system_model: term(),
  system_model_part_number: term(),
  system_status: term(),
  tags: term(),
  tags_join_assoc: term(),
  tenant: term(),
  tenant_id: term(),
  updated_at: term(),
  volume_deployments: term(),
  wifi_scan_results: term()
}
```

# `default_short_name`

# `input`

```elixir
@spec input(values :: map() | Keyword.t()) :: map() | no_return()
```

Validates that the keys in the provided input are valid for at least one action on the resource.

Raises a KeyError error at compile time if not. This exists because generally a struct should only ever
be created by Ash as a result of a successful action. You should not be creating records manually in code,
e.g `%MyResource{value: 1, value: 2}`. Generally that is fine, but often with embedded resources it is nice
to be able to validate the keys that are being provided, e.g

```elixir
Resource
|> Ash.Changeset.for_create(:create, %{embedded: EmbeddedResource.input(foo: 1, bar: 2)})
|> Ash.create()
```

# `input`

```elixir
@spec input(values :: map() | Keyword.t(), action :: atom()) :: map() | no_return()
```

Same as `input/1`, except restricts the keys to values accepted by the action provided.

# `primary_key_matches?`

