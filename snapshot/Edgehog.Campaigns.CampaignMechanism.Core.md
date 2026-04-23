# `Edgehog.Campaigns.CampaignMechanism.Core`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/campaigns/campaign_mechanism/core.ex#L21)

Protocol defining the core functions that a campaign mechanism must implement.

These functions cover the essential operations needed to manage and execute campaigns,
including operation tracking, target management, and notification handling.

# `t`

```elixir
@type t() :: term()
```

All the types that implement this protocol.

# `available_slots`

# `can_retry?`

# `do_operation`

# `error_message`

# `fetch_next_valid_target`

# `format_operation_failure_log`

# `get_campaign!`

# `get_campaign_status`

# `get_failed_target_count`

# `get_in_progress_target_count`

# `get_mechanism`

# `get_operation_id`

# `get_target!`

# `get_target_count`

# `get_target_for_operation!`

# `has_idle_targets?`

# `increase_retry_count!`

# `list_in_progress_targets`

# `mark_campaign_as_failed!`

# `mark_campaign_as_paused!`

# `mark_campaign_as_successful!`

# `mark_campaign_in_progress!`

# `mark_operation_as_timed_out!`

# `mark_target_as_failed!`

# `mark_target_as_successful!`

# `pending_request_timeout_ms`

# `retry_operation`

# `subscribe_to_operation_updates!`

# `temporary_error?`

# `unsubscribe_to_operation_updates!`

# `update_target_latest_attempt`

