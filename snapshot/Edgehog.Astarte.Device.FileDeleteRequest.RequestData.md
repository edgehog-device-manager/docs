# `Edgehog.Astarte.Device.FileDeleteRequest.RequestData`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.0/backend/lib/edgehog/astarte/device/file_delete_request/request_data.ex#L21)

Struct representing the data needed to request a file deletion on an Astarte device.

# `t`

```elixir
@type t() :: %Edgehog.Astarte.Device.FileDeleteRequest.RequestData{
  fileId: String.t(),
  force: boolean(),
  id: String.t()
}
```

