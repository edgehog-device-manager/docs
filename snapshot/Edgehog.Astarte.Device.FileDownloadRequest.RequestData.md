# `Edgehog.Astarte.Device.FileDownloadRequest.RequestData`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/astarte/device/file_download_request/request_data.ex#L21)

Struct representing the data needed to request a file download on an Astarte device.

# `t`

```elixir
@type t() :: %Edgehog.Astarte.Device.FileDownloadRequest.RequestData{
  destination: Edgehog.Files.FileDownloadRequest.FileDestination.t(),
  destinationType: String.t(),
  digest: String.t() | nil,
  encoding: String.t(),
  fileMode: non_neg_integer(),
  fileSizeBytes: non_neg_integer() | nil,
  groupId: integer(),
  httpHeaderKeys: [String.t()],
  httpHeaderValues: [String.t()],
  id: String.t(),
  progress: boolean(),
  ttlSeconds: non_neg_integer(),
  url: String.t(),
  userId: integer()
}
```

