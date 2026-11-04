# `Edgehog.Audit.Types.ActionEventInfo`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/audit/types/action_event_info.ex#L21)

Type containing all the data regarding an Ash action that triggered the creation
of an audit event.

Fields:
- resource module
- record id
- action name
- action type
- action inputs (attributes and arguments)
- attributes changed on the record (includes defaults, auto-generated values, business logic changes...)
- actor

# `t`

```elixir
@type t() :: %{
  resource_module: module(),
  record_id: integer() | String.t() | Ash.Union.t(),
  action_name: atom(),
  action_type: :create | :read | :update | :destroy | :action,
  action_inputs: map(),
  changed_attributes: map(),
  actor: map() | nil
}
```

# `handle_change?`

# `prepare_change?`

