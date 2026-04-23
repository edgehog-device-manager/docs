# `Edgehog.Astarte.Device.FileDownloadRequest.Behaviour`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/astarte/device/file_download_request/behaviour.ex#L21)

Behaviour for requesting file downloads on Astarte devices.

# `request_download`

```elixir
@callback request_download(
  client :: Astarte.Client.AppEngine.t(),
  device_id :: String.t(),
  request_data :: Edgehog.Astarte.Device.FileDownloadRequest.RequestData.t()
) :: :ok | {:error, term()}
```

