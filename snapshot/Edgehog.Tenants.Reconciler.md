# `Edgehog.Tenants.Reconciler`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.1/backend/lib/edgehog/tenants/reconciler.ex#L21)

The tenant reconciler.

This service is responsible for keeping interfaces, triggers and delivery
policies up to date and running on astarte, handling different astarte
versions.

# `child_spec`

Returns a specification to start this module under a supervisor.

See `Supervisor`.

# `name`

# `reconcile`

Reconciles a tenant.

Sends a new message to the tenant reconciler casting a `:reconcile` message.

The reconciler server for that tenant proceeds with reconciliation in a separate process.

# `reconcile_tenant`

> This function is deprecated. Tenant reconciliation should happen through the new API.

see `reconcile/1`
.

# `start_link`

# `start_reconciler`

