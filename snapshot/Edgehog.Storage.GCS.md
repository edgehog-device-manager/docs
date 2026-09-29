# `Edgehog.Storage.GCS`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/storage/gcs.ex#L21)

Google Cloud Storage backend for presigned URL generation and file management.

Presigned URLs are generated with `GcsSignedUrl`, while deletion is performed
through the S3-compatible API exposed by GCS via `ExAws`.

