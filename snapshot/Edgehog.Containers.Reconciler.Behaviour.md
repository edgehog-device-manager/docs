# `Edgehog.Containers.Reconciler.Behaviour`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/containers/reconciler/behaviour.ex#L21)

Behavior for the reconciler. It should implement
- a `start_link` to start the reconciler.
- a `register_device` to start a device timer in the reconciler.
- a `stop_device` to stop a device timer in the reconciler.

# `register_device`

```elixir
@callback register_device(
  device :: Edgehog.Devices.Device.t(),
  tenant :: Edgehog.Tenants.Tenant.t()
) :: :ok
```

# `start_link`

```elixir
@callback start_link(args :: Keyword.t()) :: GenServer.on_start()
```

# `stop_device`

```elixir
@callback stop_device(
  device :: Edgehog.Devices.Device.t(),
  tenant :: Edgehog.Tenants.Tenant.t()
) :: :ok
```

