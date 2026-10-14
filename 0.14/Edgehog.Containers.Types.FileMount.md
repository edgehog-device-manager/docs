# `Edgehog.Containers.Types.FileMount`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.0/backend/lib/edgehog/containers/types/file_mount.ex#L21)

Input type to represent a file mount.

A file mount describes how a single file should be mounted inside a
container: the path at which it should appear (`mountpoint`), whether
the container requires it to be present in order to start (`required`),
and, optionally, the file that should be used to populate it by default
(`default_file_id`).

# `handle_change?`

# `prepare_change?`

