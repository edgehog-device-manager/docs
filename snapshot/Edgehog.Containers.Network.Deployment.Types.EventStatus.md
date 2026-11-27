# `Edgehog.Containers.Network.Deployment.Types.EventStatus`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/containers/network/deployment/types/event_status.ex#L21)

Expresses the status of an event a device can communicate to the backend through the `NetworkEvent` interface.

# `t`

```elixir
@type t() ::
  :error
  | :prune
  | :remove
  | :update
  | :destroy
  | :disconnect
  | :connect
  | :create
```

# `graphql_type`

# `handle_change?`

# `prepare_change?`

