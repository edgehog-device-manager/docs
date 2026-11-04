# `Edgehog.Audit.AuditService`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/audit/audit_service.ex#L21)

Service module exposing the API to audit events across the application.

# `option`

```elixir
@type option() :: {:tenant, Edgehog.Tenants.Tenant.t() | integer() | nil}
```

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

