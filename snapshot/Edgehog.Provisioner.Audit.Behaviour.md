# `Edgehog.Provisioner.Audit.Behaviour`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/provisioner/audit/behaviour.ex#L21)

Behavior describing the Audit functions for the Provisioner.

`Audit` modules contain resource specific observability functions required by
the provisioner. Each function handles a single provisioning event and
chooses what to do (log and/or telemetry).

This module shouldn't be used directyl, instead:

```ex
defmodule ResourceProvisioner.Audit do
  use Edgehog.Provisioner.Audit
end
```

which will declare the module implements the behaviour.

# `error`

```elixir
@type error() :: term()
```

# `resource`

```elixir
@type resource() :: Edgehog.Provisioner.Behaviour.resource()
```

See `Edgehog.Provisioner.Behaviour.resource()`.

# `api_error`

```elixir
@callback api_error(resource(), error()) :: term()
```

Audits a failed send to device operation.

# `device_status`

```elixir
@callback device_status(String.t(), boolean()) :: term()
```

Audits the current device online/offline status.

# `provisioning_completed`

```elixir
@callback provisioning_completed(
  resource(),
  keyword(),
  start_metadata :: term(),
  retries :: non_neg_integer(),
  result :: term()
) :: term()
```

Audits a successful provisioning.

# `provisioning_failed`

```elixir
@callback provisioning_failed(
  resource(),
  keyword(),
  start_metadata :: term(),
  retries :: non_neg_integer(),
  reason :: term()
) :: term()
```

Audits a failed provisioning.

# `provisioning_started`

```elixir
@callback provisioning_started(
  resource(),
  keyword()
) :: term()
```

Audits the start of a provisioning.

Returns any state or metadata (e.g. start timestamp) needed for subsequent
provisioning completed or failed events.

# `sent_to_device`

```elixir
@callback sent_to_device(resource(), resource()) :: term()
```

Audits a successful send of the resource to the device.

Receives the actual resource that was sent and the device it was sent to.

# `subscribing_to_events`

```elixir
@callback subscribing_to_events(String.t()) :: term()
```

Audits the subscription to resource events on the given topic.

