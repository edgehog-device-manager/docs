# `Edgehog.Tenants.Reconciler.Core.Triggers`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.0/backend/lib/edgehog/tenants/reconciler/core/triggers.ex#L21)

The reconciler core part for triggers.

The main entrypoint is `reconcile/1`

`reconcile/1` takes as input a context and tries to install all the available
triggers based on previous steps results:

- if delivery policies are compatible builds triggers accordingly
- if astarte is compatible with device registration and deletion triggers,
  then it tries to install such triggers.

# `delete`

Uninstalls trigger from the given context.

This function takes a context (with a realm management client embedded) and
queries astarte to uninstall the given triggers

Trigger deletion happens by name, only the trigger name is actually used to
delete the trigger, hence, be careful what you wish for!

# `list_triggers`

Lists all the available triggers.

These triggers are `EEx` evaluated and can either be constructed with or without policies (by default, without).

# `reconcile`

Reconciles the triggers for a given context.

If there is any error in the interfaces scope we cannot guarantee that
interfaces have been installed. Hence, we cannot install triggers.

This also checks the compatibility with device deletion and registration
triggers.

# `reconcile_trigger`

