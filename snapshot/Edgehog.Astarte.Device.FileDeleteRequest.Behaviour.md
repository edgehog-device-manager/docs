# `Edgehog.Astarte.Device.FileDeleteRequest.Behaviour`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/astarte/device/file_delete_request/behaviour.ex#L21)

Behaviour for requesting file deletion on Astarte devices.

# `request_deletion`

```elixir
@callback request_deletion(
  client :: Astarte.Client.AppEngine.t(),
  device_id :: String.t(),
  request_data :: Edgehog.Astarte.Device.FileDeleteRequest.RequestData.t()
) :: :ok | {:error, term()}
```

