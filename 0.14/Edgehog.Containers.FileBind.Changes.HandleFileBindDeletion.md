# `Edgehog.Containers.FileBind.Changes.HandleFileBindDeletion`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.0/backend/lib/edgehog/containers/file_bind/changes/handle_file_bind_deletion.ex#L21)

Deletes the bucket object uploaded for a target-less file bind.

Bucket objects are kept after the file download request completes so
redeploys can reuse them, and are removed only when the file bind itself
is destroyed. Binds that never received an upload have nothing to delete.

