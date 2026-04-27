# `Edgehog.Files.EphemeralFile.Behaviour`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/files/file_download_request/ephemeral_file/behaviour.ex#L21)

Behaviour for handling ephemeral files used in file download requests.

# `upload`

```elixir
@type upload() :: %Plug.Upload{content_type: term(), filename: term(), path: term()}
```

# `delete`

```elixir
@callback delete(
  tenant_id :: String.t(),
  file_download_request_id :: String.t(),
  url :: String.t()
) :: :ok | {:error, reason :: any()}
```

# `upload`

```elixir
@callback upload(
  tenant_id :: String.t(),
  file_download_request_id :: String.t(),
  upload()
) ::
  {:ok, file_url :: String.t()} | {:error, reason :: any()}
```

