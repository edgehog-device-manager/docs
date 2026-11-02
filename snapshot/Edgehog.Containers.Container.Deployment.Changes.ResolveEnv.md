# `Edgehog.Containers.Container.Deployment.Changes.ResolveEnv`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/containers/container/deployment/changes/resolve_env.ex#L21)

Resolves the effective `:env` and `:env_strategy` attributes for a container
deployment by combining the template container's environment variables with
any deployment-time `:env` and `:env_strategy` overrides.

