# `Edgehog.Containers.Provisioner.Core.Behaviour`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/provisioner/core/behaviour.ex#L21)

Behaviour describing the API of the Core functions for a Provisioner.

A `Core` module contains the resource specific functions required by the
provisioner to perform the provisioning: pure functions that can be tested in
isolation, and functions that provide the side effects of the provisioning
flow (e.g. actually sending the request to the device, or reconciling the
resource state with what astarte reports).

This module shouldn't be used directly. Rather, it's best to
use `Edgehog.Containers.Provisioner.Core`, i.e.:

```ex
defmodule ResourceProvisioner.Core do
  use Edgehog.Containers.Provisioner.Core
end
```

which will declare that the module implements this behaviour. All the
functions of this behaviour must be implemented explicitly: there are no
default implementations.

# `ash_action_return`

```elixir
@type ash_action_return() ::
  {:ok, Ash.Resource.record()}
  | {:ok, Ash.Resource.record(), [Ash.Notifier.Notification.t()]}
  | {:error, term()}
```

# `error`

```elixir
@type error() :: term()
```

# `id`

```elixir
@type id() :: term()
```

# `provisioner_registry`

```elixir
@type provisioner_registry() :: term()
```

A term, usually a module-like atom, identifying a registry for the provisioners

# `reconcile_opts`

```elixir
@type reconcile_opts() :: [{:tenant, Edgehog.Tenants.Tenant.t()}]
```

# `resource`

```elixir
@type resource() :: Edgehog.Containers.Provisioner.Behaviour.resource()
```

See `Edgehog.Containers.Provisioner.Behaviour.resource()`.

# `send_to_device_opts`

```elixir
@type send_to_device_opts() :: [
  tenant: Edgehog.Tenants.Tenant.t(),
  deployment: term()
]
```

# `log_api_error`

```elixir
@callback log_api_error(resource(), error()) :: :ok
```

Logs when a send to device operation fails.

# `log_device_status`

```elixir
@callback log_device_status(String.t(), boolean()) :: :ok
```

Logs the current device online/offline status.

# `log_provisioning_completed`

```elixir
@callback log_provisioning_completed(resource(), non_neg_integer()) :: :ok
```

Logs when provisioning completes successfully for a resource.

# `log_provisioning_failed`

```elixir
@callback log_provisioning_failed(resource(), term()) :: :ok
```

Logs when provisioning fails for a resource.

# `log_provisioning_started`

```elixir
@callback log_provisioning_started(resource(), resource()) :: :ok
```

Logs when provisioning starts for a resource.

Receives the actual resource that was sent and the device it was sent to.

# `log_subscribing_to_device_status`

```elixir
@callback log_subscribing_to_device_status(String.t()) :: :ok
```

Logs when subscribing to device status events.

# `log_subscribing_to_events`

```elixir
@callback log_subscribing_to_events(String.t()) :: :ok
```

Logs when subscribing to resource events on the given topic.

# `name`

```elixir
@callback name(resource()) :: {:via, Registry, {provisioner_registry(), id()}}
```

Returns the via tuple used as the name for the provisioner on its registry.

# `ready?`

```elixir
@callback ready?(resource()) :: boolean()
```

Checks whether the resource is in a terminal (ready) state, i.e. the device
acknowledged its presence (or absence) and no further provisioning is needed.

# `reconcile`

```elixir
@callback reconcile(resource(), reconcile_opts()) :: ash_action_return() | :not_found
```

Tries to reconcile the resource with the property set by the device.

This function reads the available resources the device publishes, and either
finds a state, and sets the resource to that state or does not find a valid
state, therefore the device does not have such resource deployed, and the
function returns :not_found.

Alternatively, if something went wrong while updating the resource, an
`{:error, _}` is returned.

Example:
```elixir
Core.reconcile(resource, tenant: tenant)
> {:ok, new_resource}

Core.reconcile(resource, tenant: tenant)
> :not_found
```

# `send_to_device`

```elixir
@callback send_to_device(resource(), send_to_device_opts()) :: :ok | {:error, term()}
```

Sends the appropriate messages to the device.

It loads all the necessary data from the resource, and then calls the correct
`Edgehog.Devices.send_create_<resource_name>_request/4` function.

# `subscribe_topic`

```elixir
@callback subscribe_topic(resource()) :: String.t()
```

Returns the topic onto which the provisioner subscribes to receive the events
that the resource emits when it is updated.

# `temporary_error?`

```elixir
@callback temporary_error?(error()) :: boolean()
```

Checks whether an error returned by `send_to_device/3` from Astarte APIs is
temporary (i.e.: can be retried in a bit), or if it's not, and should thus cause
a failure of the Provisioner.

# `topic`

```elixir
@callback topic(resource()) :: String.t()
```

Returns the topic onto which the provisioner broadcasts readiness and failure
for the given resource.

