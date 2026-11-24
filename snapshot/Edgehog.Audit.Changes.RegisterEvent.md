# `Edgehog.Audit.Changes.RegisterEvent`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/audit/changes/register_event.ex#L21)

A change that registers an audit event about the create, update, destroy action
being run on the resource, through `Edgehog.Audit.AuditService`.

The event is registered after the action completed, for both success and failures,
and the auditing never fails the action.

For read or manual actions, see `Edgehog.Audit.Preparations.RegisterEvent` instead.

Opts:
- `:actor?`   :: boolean. Whether to include the actor (specified in the context, if
  any) in the registered event. Defaults to `true`.
- `:metadata` :: map, optional. the metadata to be registered with the event

