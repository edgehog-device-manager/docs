# `Edgehog.Audit.AuditService`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/audit/audit_service.ex#L21)

Service module exposing the API to audit events across the application.

# `convenience_option`

```elixir
@type convenience_option() ::
  option()
  | {:metadata, map()}
  | {:ash_action_info, Edgehog.Audit.Types.ActionEventInfo.t() | nil}
```

# `option`

```elixir
@type option() :: {:tenant, Edgehog.Tenants.Tenant.t() | integer() | nil}
```

# `debug`

```elixir
@spec debug(String.t(), [convenience_option()]) :: :ok | {:error, term()}
```

Registers an audit event at debug level.

# `error`

```elixir
@spec error(String.t(), [convenience_option()]) :: :ok | {:error, term()}
```

Registers an audit event at error level.

# `info`

```elixir
@spec info(String.t(), [convenience_option()]) :: :ok | {:error, term()}
```

Registers an audit event at info level.

# `register_event`

```elixir
@spec register_event(
  message :: String.t(),
  log_level :: Logger.level(),
  ash_action_info :: Edgehog.Audit.Types.ActionEventInfo.t() | nil,
  metadata :: map(),
  opts :: [option()]
) :: :ok | {:error, term()}
```

Registers an event by logging the given message and creating an `Edgehog.Audit.Event`
resource, if configured.

# `warning`

```elixir
@spec warning(String.t(), [convenience_option()]) :: :ok | {:error, term()}
```

Registers an audit event at warning level.
