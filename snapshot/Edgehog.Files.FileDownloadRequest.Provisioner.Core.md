# `Edgehog.Files.FileDownloadRequest.Provisioner.Core`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/files/file_download_request/provisioner/core.ex#L21)

The module describing the Core functions required by the file download
request provisioner.

It allows the container deployment orchestrator to wait for the files
backing target-less file binds like any other provisioned resource: the
provisioner broadcasts readiness once the device reports the download as
completed, and a failure if the provisioning deadline is hit.

For more information, check the `Edgehog.Containers.Provisioner.Core.Behaviour` docs.

