# `Edgehog.Containers.Container.Deployment.Types.EventStatus`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/containers/container/deployment/types/event_status.ex#L21)

Expresses the status of an event a device can communicate to the backend through the `ContainerEvent` interface.

# `t`

```elixir
@type t() ::
  :error
  | :update
  | :unpause
  | :top
  | :resize
  | :rename
  | :pause
  | :health_status
  | :export
  | :exec_die
  | :exec_start
  | :exec_detach
  | :exec_create
  | :detach
  | :copy
  | :commit
  | :attach
  | :oom
  | :prune
  | :destroy
  | :kill
  | :die
  | :stop
  | :restart
  | :start
  | :create
```

# `graphql_type`

# `handle_change?`

# `prepare_change?`

