# `Edgehog.Astarte.Device.FileUploadRequest.Behaviour`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/astarte/device/file_upload_request/behaviour.ex#L21)

Behaviour for requesting file uploads on Astarte devices.

# `request_upload`

```elixir
@callback request_upload(
  client :: Astarte.Client.AppEngine.t(),
  device_id :: String.t(),
  request_data :: Edgehog.Astarte.Device.FileUploadRequest.RequestData.t()
) :: :ok | {:error, term()}
```

