# `Edgehog.Containers.EnvFile.Changes.HandleEnvFileDeletion`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/env_file/changes/handle_env_file_deletion.ex#L20)

Deletes the bucket object uploaded for a target-less env file.

Bucket objects are kept after the file download request completes so
redeploys can reuse them, and are removed only when the env file itself
is destroyed. Env files that never received an upload have nothing to delete.

