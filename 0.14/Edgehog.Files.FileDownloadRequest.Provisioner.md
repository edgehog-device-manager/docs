# `Edgehog.Files.FileDownloadRequest.Provisioner`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.0/backend/lib/edgehog/files/file_download_request/provisioner.ex#L21)

The provisioner for file download requests backing container file binds.

It waits until the device reports the download as completed, so the
container deployment orchestrator can treat files like any other
provisioned resource.

For more information, check the `Edgehog.Containers.Provisioner` docs.

# `child_spec`

Returns a specification to start this module under a supervisor.

See `Supervisor`.

