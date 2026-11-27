# `Edgehog.Containers.Image.Deployment.Types.EventStatus`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/containers/image/deployment/types/event_status.ex#L21)

Expresses the status of an event a device can communicate to the backend through the `ImageEvent` interface.

# `t`

```elixir
@type t() ::
  :error
  | :prune
  | :untag
  | :tag
  | :save
  | :push
  | :pull
  | :load
  | :import
  | :delete
  | :create
```

# `graphql_type`

# `handle_change?`

# `prepare_change?`

