# `Edgehog.Campaigns.CampaignMechanism.DeploymentDeploy`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/campaigns/campaign_mechanism/deployment_deploy/deployment_deploy.ex#L21)

Defines the Deploy Campaign Mechanism resource.
This resource represents the configuration for a deploy operation within a deployment campaign.

An object representing the properties of a Deploy deployment campaign mechanism.

# `t`

```elixir
@type t() :: %Edgehog.Campaigns.CampaignMechanism.DeploymentDeploy{
  __lateral_join_source__: term(),
  __meta__: term(),
  __metadata__: term(),
  __order__: term(),
  aggregates: term(),
  calculations: term(),
  max_failure_percentage: term(),
  max_in_progress_operations: term(),
  release: term(),
  release_id: term(),
  request_retries: term(),
  request_timeout_seconds: term(),
  type: term()
}
```

# `apply_constraints_array`

# `cast_input`

# `cast_stored`

# `check_atomic`

# `default_short_name`

# `dump_to_native`

# `equal?`

# `fetch_key`

# `get_rewrites`

# `handle_change`

# `handle_change?`

# `handle_change_array`

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

# `load`

# `prepare_change`

# `prepare_change?`

# `prepare_change_array`

# `rewrite`

# `storage_type`

