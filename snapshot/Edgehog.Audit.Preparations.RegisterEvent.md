# `Edgehog.Audit.Preparations.RegisterEvent`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/audit/preparations/register_event.ex#L21)

A preparation that registers an audit event about the manual action
being run on the resource, through `Edgehog.Audit.AuditService`.

The event is registered after the action completed, for both success and failures,
and the auditing never fails the action.

Read actions are currently not implemented.
For create, update and destroy actions, see `Edgehog.Audit.Changes.RegisterEvent`
instead.

Opts:
- `:actor?`   :: boolean. Whether to include the actor (present in the context,
  if any) in the registered event. Defaults to `true`.
- `:metadata` :: map, optional. the metadata to be registered with the event,
  which can also include information usually returned by other action types,
  like a record id created or edited through the action

# `temporal_safe?`

