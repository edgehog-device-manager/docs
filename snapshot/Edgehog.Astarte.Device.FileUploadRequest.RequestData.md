# `Edgehog.Astarte.Device.FileUploadRequest.RequestData`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/astarte/device/file_upload_request/request_data.ex#L21)

Struct representing the data needed to request a file upload on an Astarte device.

# `t`

```elixir
@type t() :: %Edgehog.Astarte.Device.FileUploadRequest.RequestData{
  encoding: String.t(),
  httpHeaderKeys: [String.t()],
  httpHeaderValues: [String.t()],
  id: String.t(),
  progress: boolean(),
  source: String.t(),
  sourceType: String.t(),
  url: String.t()
}
```

