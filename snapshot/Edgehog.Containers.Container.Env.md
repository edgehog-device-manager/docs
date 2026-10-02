# `Edgehog.Containers.Container.Env`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.0/backend/lib/edgehog/containers/container/env.ex#L21)

Helpers to resolve and encode the environment variables of a container.

# `encode`

Encodes a list of environment variables into the `KEY=VALUE` format expected
by the device.

# `resolve`

Resolves the effective environment variables of a container given the
environment configured on the container itself and the one provided at deploy
time.

When the strategy is `:merge`, the deploy-time variables are appended to the
container ones, with the deploy-time variables winning on duplicate keys.
When the strategy is `:override`, the deploy-time variables fully replace the
container ones.

