# `Edgehog.Tenants.Reconciler.Starter`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.1/backend/lib/edgehog/tenants/reconciler/starter.ex#L19)

Tenant reconciler starter.

At application start this server reads all the tenants available in the db and starts their reconcilers.

# `child_spec`

Returns a specification to start this module under a supervisor.

See `Supervisor`.

# `start_link`

