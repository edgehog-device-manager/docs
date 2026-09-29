# `Edgehog.Containers.EnvFile.Provisioner.Core`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/env_file/provisioner/core.ex#L20)

The module describing the Core functions required by the env file provisioner.

Provisioning an env file means creating the file download request backing
an uploaded file when the env file has no explicit target, and then sending a
`CreateEnvFileRequest` to the device. Readiness is reported by the device
through the `AvailableEnvFiles` interface, like any other container
resource.

For more information, check the `Edgehog.Containers.Provisioner.Core.Behaviour` docs.

# `maybe_update`

