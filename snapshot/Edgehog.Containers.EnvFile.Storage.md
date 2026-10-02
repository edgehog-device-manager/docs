# `Edgehog.Containers.EnvFile.Storage`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.0/backend/lib/edgehog/containers/env_file/storage.ex#L20)

Storage helpers for target-less env files.

Objects live under `uploads/tenants/<tenant_id>/env_files/<env_file_id>/file`.
The object key intentionally does not depend on the file name, since the
name is only known when the upload is marked as uploaded, while the
presigned upload URL is read before that.

Objects are kept after the file download request completes so redeploys can
reuse them. They are deleted when the env file is destroyed.

# `create_presigned_urls`

# `delete`

# `file_path`

# `read_presigned_url`

