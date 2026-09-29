# `Edgehog.Containers.Container.Deployment.Validations.EnvOrEnvFile`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/container/deployment/validations/env_or_env_file.ex#L20)

Ensures that a container deployment does not have both additional env vars and env files.
At most one of `env` and `env_files` may be set; setting both is ambiguous.
`none` (both empty) is allowed to inherit the image defaults.

