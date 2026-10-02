# `Edgehog.Containers.FileBind.Provisioner.Core`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.0/backend/lib/edgehog/containers/file_bind/provisioner/core.ex#L21)

The module describing the Core functions required by the file bind provisioner.

Provisioning a file bind means creating the file download request backing
an uploaded file when the bind has no explicit target, and then sending a
`CreateFileBindRequest` to the device. Readiness is reported by the device
through the `AvailableFileBinds` interface, like any other container
resource.

For more information, check the `Edgehog.Containers.Provisioner.Core.Behaviour` docs.

# `maybe_update`

