# `Edgehog.Containers.Validations.ContainsFile`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/validations/contains_file.ex#L21)

Edgehog validation on FileBind input types.

Checks that a file bind (or a list of file binds) does not reference both
a file download request and a device file at the same time. A file bind
without any target is valid and represents a pending upload.

