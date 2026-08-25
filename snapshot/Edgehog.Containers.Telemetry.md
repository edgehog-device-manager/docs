# `Edgehog.Containers.Telemetry`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/telemetry.ex#L21)

Emits the telemetry events of the containers feature.

Events can be emitted on the following topics:

- `[:edgehog, :containers, :provisioning, :start]` when a provisioner
  starts provisioning a resource. Metadata contains `resource_type`,
  `resource_id`, `deployment_id` and `device_id`.
- `[:edgehog, :containers, :provisioning, :stop]` when a provisioner
  terminates, either successfully or with a failure. Metadata contains
  `resource_type`, `resource_id`, `deployment_id`, `device_id`, `result`
  (either `:ok` or `:error`) and `reason` (either the provisioning outcome,
  e.g. `:ready` or `:already_ready`, or the failure reason). Measurements
  contain `duration` (native time) and `retries`.
- `[:edgehog, :containers, :deployment, :start]` when a deployment
  orchestrator starts conducting a deployment. Metadata contains
  `deployment_id` and `device_id`.
- `[:edgehog, :containers, :deployment, :stop]` when a deployment
  orchestrator terminates, either successfully or with a failure. Metadata
  contains `deployment_id`, `device_id` and `result`. Measurements contain
  `duration` (native time).
- `[:edgehog, :containers, :container_deployment, :start]` when a container
  deployment orchestrator starts conducting a container deployment. Metadata
  contains `container_deployment_id`, `deployment_id` and `device_id`.
- `[:edgehog, :containers, :container_deployment, :stop]` when a container
  deployment orchestrator terminates, either successfully or with a failure.
  Metadata contains `container_deployment_id`, `deployment_id`, `device_id`
  and `result`. Measurements contain `duration` (native time).

# `container_deployment_completed`

Emits a successful container deployment orchestration stop event.

# `container_deployment_failed`

Emits a failed container deployment orchestration stop event.

# `container_deployment_start_event`

# `container_deployment_started`

Emits a container deployment orchestration start event and returns the
monotonic time the orchestration started, to be used when emitting the
corresponding stop event.

Returns the start time, computed with `System.monotonic_time/0`

# `container_deployment_stop_event`

# `deployment_completed`

Emits a successful deployment orchestration stop event.

# `deployment_failed`

Emits a failed deployment orchestration stop event.

# `deployment_start_event`

# `deployment_started`

Emits a deployment orchestration start event and returns the monotonic time
the orchestration started, to be used when emitting the corresponding stop
event.

Returns the start time, computed with `System.monotonic_time/0`

# `deployment_stop_event`

# `include_identifiers?`

# `provisioning_completed`

Emits a successful provisioning stop event.

# `provisioning_failed`

Emits a failed provisioning stop event.

# `provisioning_start_event`

# `provisioning_started`

Emits a provisioning start event and returns the monotonic time the
provisioning started, to be used when emitting the corresponding stop event.

Returns the start time, computed with `System.monotonic_time/0`

# `provisioning_stop_event`

# `resource_type`

