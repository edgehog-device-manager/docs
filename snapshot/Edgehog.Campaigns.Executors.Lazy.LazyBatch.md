# `Edgehog.Campaigns.Executors.Lazy.LazyBatch`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/campaigns/executors/lazy/lazy_batch.ex#L21)

Generic lazy batch executor for campaigns using a macro-based approach.

# `handle_info`

```elixir
@callback handle_info(
  message :: term(),
  state :: atom(),
  data :: %Edgehog.Campaigns.Executors.Lazy.LazyBatch{
    available_slots: term(),
    campaign_id: term(),
    failed_count: term(),
    in_progress_count: term(),
    mechanism: term(),
    target_count: term(),
    tenant_id: term()
  }
) :: :gen_statem.event_handler_result(:state_enter)
```

Callback for handling `:info` messages.

This callback is invoked when the executor receives a message.
Implementing modules should pattern match on the message and return
the same result type as `GenStateMachine.handle_event/4`.

# `add_failure`

# `cancel_retry_timeout`

# `failure_threshold_exceeded?`

# `free_up_slot`

# `handle_event`

Handles all GenStateMachine events. This function is called by the using module's
`handle_event/4` callback.

# `internal_event`

# `occupy_slot`

# `setup_retry_timeout`

# `slot_available?`

# `targets_in_progress?`

# `terminate_executor`

