# `Edgehog.Containers.Container.Deployment.Changes.RelateEnvFiles`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/containers/container/deployment/changes/relate_env_files.ex#L21)

Attaches the target `:device_id` to each entry in the `:env_files` argument
and relates them to the container deployment via `manage_relationship/4`.

