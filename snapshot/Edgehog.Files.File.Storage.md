# `Edgehog.Files.File.Storage`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/files/file/storage.ex#L21)

Behaviour for file storage implementations.

# `encoding`

```elixir
@type encoding() :: nil | :gz | :lz4
```

# `upload`

```elixir
@type upload() :: %Plug.Upload{content_type: term(), filename: term(), path: term()}
```

# `delete`

```elixir
@callback delete(
  file :: %Edgehog.Files.File{
    __lateral_join_source__: term(),
    __meta__: term(),
    __metadata__: term(),
    __order__: term(),
    aggregates: term(),
    base_file: term(),
    calculations: term(),
    gz_file: term(),
    id: term(),
    inserted_at: term(),
    is_archive: term(),
    lz4_file: term(),
    name: term(),
    repository: term(),
    repository_id: term(),
    size: term(),
    tenant: term(),
    tenant_id: term(),
    updated_at: term()
  },
  encoding :: encoding()
) :: :ok | {:error, reason :: any()}
```

# `store`

```elixir
@callback store(
  tenant_id :: String.t() | integer(),
  file_name :: String.t(),
  repository_id :: String.t() | integer(),
  encoding :: encoding(),
  file :: upload()
) :: {:ok, file_url :: String.t()} | {:error, reason :: any()}
```

