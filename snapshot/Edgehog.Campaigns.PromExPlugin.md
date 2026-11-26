# `Edgehog.Campaigns.PromExPlugin`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/campaigns/prom_ex_plugin.ex#L21)

PromEx plugin for the Edgehog campaigns feature.

Every metric is a counter updated when a campaign starts, labeled by
`tenant_slug` and `mechanism_type`:

- `edgehog_campaigns_started_total`
- `edgehog_campaigns_targets_total`: targets of the started campaigns
- `edgehog_campaigns_max_in_progress_operations_total`: targets that can be
  active at the same time, summed over the started campaigns
- `edgehog_campaigns_target_groups_total`: groups targeted by the started
  campaigns
- `edgehog_campaigns_max_retries_total`: `request_retries` summed over the
  started campaigns
- `edgehog_campaigns_max_failure_percentage_total`: `max_failure_percentage`
  summed over the started campaigns

The averages per campaign are obtained dividing a metric by
`edgehog_campaigns_started_total`.

