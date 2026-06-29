# `Edgehog.Containers.Deployment.Types.DeploymentContext`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.1/backend/lib/edgehog/containers/deployment/types/deployment_context.ex#L21)

Deployment context. An auxiliary type to track requests and pending operations on a deployment.

# `t`

```elixir
@type t() ::
  :delete_message_sent
  | :upgrade_message_sent
  | :stop_message_sent
  | :start_message_sent
```

# `handle_change?`

# `prepare_change?`

