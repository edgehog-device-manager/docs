# `Edgehog.Containers.PromExPlugin`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/prom_ex_plugin.ex#L21)

PromEx plugin for the Edgehog containers feature.

Exposes the following metric groups:

- `:containers_provisioning_event_metrics` exposing, for every resource type
  provisioned on a device (image deployments, volume deployments, network
  deployments, device mapping deployments, device request deployments,
  container deployments and deployments), the provisioning lifecycle:
  - `edgehog_containers_provisioning_started_total`
  - `edgehog_containers_provisioning_completed_total` (labeled by `result`)
  - `edgehog_containers_provisioning_duration_seconds` (labeled by `result`)
  - `edgehog_containers_provisioning_retries`

- `:containers_deployment_event_metrics` exposing the end-to-end lifecycle of
  an application deployment:
  - `edgehog_containers_deployment_started_total`
  - `edgehog_containers_deployment_completed_total` (labeled by `result`)
  - `edgehog_containers_deployment_duration_seconds`

- `:containers_container_deployment_event_metrics` exposing the lifecycle of a
  single container deployment:
  - `edgehog_containers_container_deployment_started_total`
  - `edgehog_containers_container_deployment_completed_total` (labeled by `result`)
  - `edgehog_containers_container_deployment_duration_seconds`

The provisioning metrics carry `resource_type`, `result` and `reason` labels,
which are low cardinality. Additionally, unless the
`:containers_telemetry_include_identifiers` configuration option is set to
`false`, the metrics also carry the high cardinality identifier labels
`deployment_id`, `resource_id` and `device_id`, so that the metrics can be
filtered per specific deployment, resource or device in Grafana (e.g. using a
dashboard variable resolved to the device ids of a device group).

