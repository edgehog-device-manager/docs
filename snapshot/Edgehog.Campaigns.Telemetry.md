# `Edgehog.Campaigns.Telemetry`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/campaigns/telemetry.ex#L21)

Emits the telemetry events of the campaigns feature.

Events can be emitted on the following topics:

- `[:edgehog, :campaigns, :campaign, :started]` when a campaign starts,
  i.e. when its configuration is frozen and its targets begin to receive
  operations. Measurements contain `count` (always `1`), `targets` (number
  of targets), `max_in_progress_operations` (number of targets that can be
  active at the same time), `target_groups` (number of device groups of the
  campaign channel), `max_retries` (the `request_retries` of the mechanism)
  and `max_failure_percentage` (rounded to a whole percent). Metadata contains `tenant_slug`,
  `mechanism_type`, `request_retries`, `request_timeout_seconds`.

# `campaign_started`

Emits the campaign started event.

The campaign must have the `:tenant`, `:total_target_count` and
`channel: :target_groups` fields loaded.

# `campaign_started_event`

