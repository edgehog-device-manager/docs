# `Edgehog.Storage`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/storage.ex#L21)

Storage-agnostic presigned URL generation and file management.

Dispatches to S3 or Azure backend based on the configured `:storage_type`.

# `bucket!`

Returns the configured storage bucket/container name.

# `create_presigned_urls`

Generates presigned GET and PUT URLs for a given file path.

Returns `{:ok, %{get_url: url, put_url: url}}`.

# `delete`

Deletes a file at the given path from the configured storage backend.

Returns `:ok` on success or `{:error, reason}` on failure.

# `read_presigned_url`

Generates a presigned GET URL for a given file path.

Returns `{:ok, %{get_url: url}}`.

