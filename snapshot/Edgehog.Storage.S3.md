# `Edgehog.Storage.S3`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/storage/s3.ex#L21)

AWS S3 backend for presigned URL generation and file management.

Uses the external (public) host configured in `:s3_presign_host_config` so
that generated presigned URLs are reachable by clients outside the cluster.

