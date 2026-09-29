# `Edgehog.Storage`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/storage.ex#L21)

Storage-agnostic presigned URL generation and file management.

Dispatches to the S3, Google Cloud Storage or Azure backend based on the
configured `:storage_type`.

# `bucket!`

Returns the configured storage bucket/container name.

