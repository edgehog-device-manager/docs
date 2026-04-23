# `Edgehog.Campaigns.CampaignTarget`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/campaigns/campaign_target/campaign_target.ex#L21)

Represents a CampaignTarget.

Campaign targets are the targets of a Campaign, which is composed
by the target device and the state of the target in the linked
Campaign

Represents a CampaignTarget.

Campaign targets are the targets of a Campaign, which is composed
by the target device and the state of the target in the linked
Campaign

# `t`

```elixir
@type t() :: %Edgehog.Campaigns.CampaignTarget{
  __lateral_join_source__: term(),
  __meta__: term(),
  __metadata__: term(),
  __order__: term(),
  aggregates: term(),
  calculations: term(),
  campaign: term(),
  campaign_id: term(),
  completion_timestamp: term(),
  deployment: term(),
  deployment_id: term(),
  device: term(),
  device_id: term(),
  file_download_request: term(),
  file_download_request_id: term(),
  id: term(),
  inserted_at: term(),
  latest_attempt: term(),
  ota_operation: term(),
  ota_operation_id: term(),
  retry_count: term(),
  status: term(),
  tenant: term(),
  tenant_id: term(),
  updated_at: term()
}
```

# `default_short_name`

# `input`

```elixir
@spec input(values :: map() | Keyword.t()) :: map() | no_return()
```

Validates that the keys in the provided input are valid for at least one action on the resource.

Raises a KeyError error at compile time if not. This exists because generally a struct should only ever
be created by Ash as a result of a successful action. You should not be creating records manually in code,
e.g `%MyResource{value: 1, value: 2}`. Generally that is fine, but often with embedded resources it is nice
to be able to validate the keys that are being provided, e.g

```elixir
Resource
|> Ash.Changeset.for_create(:create, %{embedded: EmbeddedResource.input(foo: 1, bar: 2)})
|> Ash.create()
```

# `input`

```elixir
@spec input(values :: map() | Keyword.t(), action :: atom()) :: map() | no_return()
```

Same as `input/1`, except restricts the keys to values accepted by the action provided.

# `primary_key_matches?`

