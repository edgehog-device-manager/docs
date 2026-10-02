# `Edgehog.Containers.FileBind.Calculations.GetUploadUrl`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.0/backend/lib/edgehog/containers/file_bind/calculations/get_upload_url.ex#L21)

Returns a presigned PUT URL the client can use to upload the file
for a target-less file bind.

The object key is `uploads/tenants/<tenant_id>/file_binds/<file_bind_id>/file`.
The object is kept in the bucket after the download request completes so
redeploys can reuse it. It is deleted when the file bind is destroyed.

# `describe`

# `has_calculate?`

# `has_expression?`

# `init`

# `strict_loads?`

