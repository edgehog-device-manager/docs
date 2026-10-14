# `Edgehog.Containers.Types.EnvStrategy`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.0/backend/lib/edgehog/containers/types/env_strategy.ex#L21)

The environment strategy to apply to a deployment configuration.

Accepts both the lowercase atoms (`:merge`/`:override`) and the
upper-case string forms (e.g. `"MERGE"`) used by GraphQL clients.

# `t`

```elixir
@type t() :: :override | :merge
```

# `handle_change?`

# `prepare_change?`

