# `Edgehog.Files.FileDownloadRequest.Status`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/files/file_download_request/status.ex#L21)

Status of a file transfer request.

Lifecycle:
  pending -> sent -> in_progress -> completed
                                -> failed
                 -> failed

# `t`

```elixir
@type t() :: :failed | :completed | :in_progress | :sent | :pending
```

# `graphql_type`

# `handle_change?`

# `prepare_change?`

