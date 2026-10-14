# `Edgehog.Containers.FileBind.Provisioner`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.0/backend/lib/edgehog/containers/file_bind/provisioner.ex#L21)

The provisioner for file binds.

Provisioning a file bind means ensuring the backing file is available on
the device (creating a file download request for uploaded files when
needed) and then sending a `CreateFileBindRequest` to the device.

For more information, check the `Edgehog.Containers.Provisioner` docs.

# `child_spec`

Returns a specification to start this module under a supervisor.

See `Supervisor`.

