# `Edgehog.Containers.Reconciler.Core`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/containers/reconciler/core.ex#L19)

Core component for the reconciler, provides `reconcile` function.

# `online_devices`

Returns online the number of online devices and a stream that contains them.

# `reconcile`

```elixir
@spec reconcile(%{device_id: integer(), tenant: Edgehog.Tenants.Tenant.t()}) ::
  :ok | {:error, term()}
```

# `reconcile_containers`

# `reconcile_deployments`

# `reconcile_device_mappings`

# `reconcile_images`

# `reconcile_networks`

# `reconcile_volumes`

