# `Edgehog.Files.FileDeleteRequest.Status`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.1/backend/lib/edgehog/files/file_delete_request/status.ex#L21)

Status of a file delete request.

Lifecycle:
  pending -> sent -> completed
               -> failed

# `t`

```elixir
@type t() :: :failed | :completed | :sent | :pending
```

# `graphql_type`

# `handle_change?`

# `prepare_change?`

