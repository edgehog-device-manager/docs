# `Edgehog.Containers.EnvFile.Calculations.GetUploadUrl`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/env_file/calculations/get_upload_url.ex#L20)

Returns a presigned PUT URL the client can use to upload the file
for a target-less env file.

The object key is `uploads/tenants/<tenant_id>/env_files/<env_file_id>/file`.
The object is kept in the bucket after the download request completes so
redeploys can reuse it. It is deleted when the env file is destroyed.

# `describe`

# `has_calculate?`

# `has_expression?`

# `init`

# `strict_loads?`

