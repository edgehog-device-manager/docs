# `Edgehog.Campaigns`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/campaigns/campaigns.ex#L21)

The Campaigns context.

# `aggregate`

> This function is deprecated. Use `Ash.aggregate/3` instead.

# `aggregate!`

> This function is deprecated. Use `Ash.aggregate!/3` instead.

# `avg`

> This function is deprecated. Use `Ash.avg/3` instead.

# `avg!`

> This function is deprecated. Use `Ash.avg!/3` instead.

# `bulk_create`

> This function is deprecated. Use `Ash.bulk_create/4` instead.

# `bulk_create!`

> This function is deprecated. Use `Ash.bulk_create!/4` instead.

# `bulk_destroy`

> This function is deprecated. Use `Ash.bulk_destroy/4` instead.

# `bulk_destroy!`

> This function is deprecated. Use `Ash.bulk_destroy!/4` instead.

# `bulk_update`

> This function is deprecated. Use `Ash.bulk_update/4` instead.

# `bulk_update!`

> This function is deprecated. Use `Ash.bulk_update!/4` instead.

# `calculate`

> This function is deprecated. Use `Ash.calculate/3` instead.

# `calculate!`

> This function is deprecated. Use `Ash.calculate!/3` instead.

# `can`

> This function is deprecated. Use `Ash.can/3` instead.

```elixir
@spec can(
  action_or_query_or_changeset ::
    Ash.Query.t()
    | Ash.Changeset.t()
    | {Ash.Resource.t(), atom() | Ash.Resource.Actions.action()},
  actor :: term(),
  opts :: Keyword.t()
) ::
  {:ok, boolean() | :maybe}
  | {:ok, true, Ash.Changeset.t() | Ash.Query.t()}
  | {:ok, true, Ash.Changeset.t(), Ash.Query.t()}
  | {:ok, false, Exception.t()}
  | {:error, term()}
```

# `can?`

> This function is deprecated. Use `Ash.can?/3` instead.

```elixir
@spec can?(
  query_or_changeset_or_action ::
    Ash.Query.t()
    | Ash.Changeset.t()
    | {Ash.Resource.t(), atom() | Ash.Resource.Actions.action()},
  actor :: term(),
  opts :: Keyword.t()
) :: boolean() | no_return()
```

# `can_fetch_campaign`

Runs authorization checks for `Edgehog.Campaigns.Campaign.read`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_fetch_campaign?`

Runs authorization checks for `Edgehog.Campaigns.Campaign.read`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_fetch_next_valid_target`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.next_valid_target`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_fetch_next_valid_target?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.next_valid_target`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_fetch_next_valid_target_with_application_deployed`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.next_valid_target_with_application_deployed`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_fetch_next_valid_target_with_application_deployed?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.next_valid_target_with_application_deployed`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_fetch_target`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.read`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_fetch_target?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.read`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_fetch_target_by_deployment`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.read`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_fetch_target_by_deployment?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.read`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_fetch_target_by_device_and_campaign`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.read`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_fetch_target_by_device_and_campaign?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.read`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_increase_target_retry_count`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.increase_retry_count`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_increase_target_retry_count?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.increase_retry_count`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_link_deployment`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.link_deployment`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_link_deployment?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.link_deployment`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_list_in_progress_targets`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.read_in_progress_targets`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_list_in_progress_targets?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.read_in_progress_targets`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_list_targets_with_pending_file_download_request`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.read_targets_with_pending_file_download_request`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_list_targets_with_pending_file_download_request?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.read_targets_with_pending_file_download_request`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_list_targets_with_pending_ota_operation`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.read_targets_with_pending_ota_operation`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_list_targets_with_pending_ota_operation?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.read_targets_with_pending_ota_operation`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_mark_campaign_failed`

Runs authorization checks for `Edgehog.Campaigns.Campaign.mark_as_failed`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_mark_campaign_failed?`

Runs authorization checks for `Edgehog.Campaigns.Campaign.mark_as_failed`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_mark_campaign_in_progress`

Runs authorization checks for `Edgehog.Campaigns.Campaign.mark_as_in_progress`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_mark_campaign_in_progress?`

Runs authorization checks for `Edgehog.Campaigns.Campaign.mark_as_in_progress`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_mark_campaign_paused`

Runs authorization checks for `Edgehog.Campaigns.Campaign.mark_as_paused`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_mark_campaign_paused?`

Runs authorization checks for `Edgehog.Campaigns.Campaign.mark_as_paused`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_mark_campaign_successful`

Runs authorization checks for `Edgehog.Campaigns.Campaign.mark_as_successful`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_mark_campaign_successful?`

Runs authorization checks for `Edgehog.Campaigns.Campaign.mark_as_successful`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_mark_target_as_failed`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.mark_as_failed`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_mark_target_as_failed?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.mark_as_failed`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_mark_target_as_in_progress`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.mark_as_in_progress`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_mark_target_as_in_progress?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.mark_as_in_progress`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_mark_target_as_successful`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.mark_as_successful`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_mark_target_as_successful?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.mark_as_successful`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_pause_campaign`

Runs authorization checks for `Edgehog.Campaigns.Campaign.pause`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_pause_campaign?`

Runs authorization checks for `Edgehog.Campaigns.Campaign.pause`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_resume_campaign`

Runs authorization checks for `Edgehog.Campaigns.Campaign.resume`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_resume_campaign?`

Runs authorization checks for `Edgehog.Campaigns.Campaign.resume`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_set_target_deployment`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.set_deployment`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_set_target_deployment?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.set_deployment`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_start_file_download`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.start_file_download`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_start_file_download?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.start_file_download`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_start_fw_upgrade`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.start_fw_upgrade`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_start_fw_upgrade?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.start_fw_upgrade`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_update_target_latest_attempt`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.update_latest_attempt`

See `Ash.can/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `can_update_target_latest_attempt?`

Runs authorization checks for `Edgehog.Campaigns.CampaignTarget.update_latest_attempt`, returning a boolean.

See `Ash.can?/3` for more information

## Options

* `:maybe_is` (`t:term/0`) - If the actor *may* be able to perform the action, what value should be returned. The default value is `:maybe`.

* `:filter_with` - If set to `:error`, the query will raise an error on a match. If set to `:filter` the query will filter out unauthorized access. Valid values are :filter, :error The default value is `:filter`.

* `:validate?` (`t:boolean/0`) - Whether or not to treat an invalid action as a non-allowed action. The default value is `false`.

* `:reuse_values?` (`t:boolean/0`) - Whether or not loaded data like aggregates, calculations and relationships should be checked in memory if possible, instead of querying. No effect if `pre_flight?` is `false`. The default value is `false`.

* `:pre_flight?` (`t:boolean/0`) - Whether or not this is a pre_flight check (which may perform optimized in-memory checks) or the final proper check. The default value is `true`.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Provides a default tenant and deep merges context (explicit opts take precedence). The actor is always taken from the second argument to `can/3`. See `Ash.Scope` for more.

* `:context` (`t:map/0`) - Context to set on the query/changeset/action_input being authorized

* `:run_queries?` (`t:boolean/0`) - Whether or not to run queries. If set to `true`, `:maybe` will not be returned. The default value is `true`.

* `:data` - The record or records specifically attempting to be acted upon.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant to use for authorization

* `:alter_source?` (`t:boolean/0`) - If set to `true`, the source being authorized is returned so it can be run. The default value is `false`.

* `:base_query` (`t:term/0`) - A base query on which to apply an generated filters

* `:no_check?` (`t:boolean/0`) - Whether or not authorization must pass at the strict/filter step, or if post-checks are allowed to be run The default value is `false`.

* `:on_must_pass_strict_check` (`t:term/0`) - Override the value returned when `no_check?` is `true` but a check must be run.

* `:atomic_changeset` (`t:term/0`) - A base query on which to apply an generated filters

* `:return_forbidden_error?` (`t:boolean/0`) - Whether or not to return a forbidden error in cases of not being authorized. The default value is `false`.

* `:log?` (`t:boolean/0`) - Whether or not to log the authorization result. The default value is `false`.

# `changeset_to_increase_target_retry_count`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_link_deployment`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_mark_campaign_failed`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_mark_campaign_in_progress`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_mark_campaign_paused`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_mark_campaign_successful`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_mark_target_as_failed`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_mark_target_as_in_progress`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_mark_target_as_successful`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_pause_campaign`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_resume_campaign`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_set_target_deployment`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_start_file_download`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_start_fw_upgrade`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_update_target_latest_attempt`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `count`

> This function is deprecated. Use `Ash.count/2` instead.

# `count!`

> This function is deprecated. Use `Ash.count!/2` instead.

# `create`

> This function is deprecated. Use `Ash.create/2` instead.

# `create!`

> This function is deprecated. Use `Ash.create!/2` instead.

# `default_short_name`

# `destroy`

> This function is deprecated. Use `Ash.destroy/2` instead.

# `destroy!`

> This function is deprecated. Use `Ash.destroy!/2` instead.

# `exists`

> This function is deprecated. Use `Ash.exists/2` instead.

# `exists?`

> This function is deprecated. Use `Ash.exists?/2` instead.

# `fetch_campaign`

Calls the read action on Edgehog.Campaigns.Campaign.

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `fetch_campaign!`

Calls the read action on Edgehog.Campaigns.Campaign.

Raises any errors instead of returning them

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `fetch_next_valid_target`

Returns the next valid target.
The next valid target is chosen with these criteria:
- It must be idle.
- It must be online.
- It must either not have been attempted before or it has to be the least
recently attempted target, in this order of preference.

This set of constraints guarantees that when we make an attempt on a
target that fails with a temporary error, given we update latest_attempt,
we can read the next updatable target to attempt updates on other
targets, or retry the same target if it is the only updatable one.

# Arguments

* campaign_id

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `fetch_next_valid_target!`

Returns the next valid target.
The next valid target is chosen with these criteria:
- It must be idle.
- It must be online.
- It must either not have been attempted before or it has to be the least
recently attempted target, in this order of preference.

This set of constraints guarantees that when we make an attempt on a
target that fails with a temporary error, given we update latest_attempt,
we can read the next updatable target to attempt updates on other
targets, or retry the same target if it is the only updatable one.

Raises any errors instead of returning them

# Arguments

* campaign_id

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `fetch_next_valid_target_with_application_deployed`

Returns the next valid target whose device has a specific application deployed.

The next valid target is chosen with these criteria:
- Must be idle
- Must be online
- Must have the specified application deployed
- It must either not have been attempted before or it has to be the least
recently attempted target, in this order of preference.

This set of constraints guarantees that when we make an attempt on a
target that fails with a temporary error, given we update latest_attempt,
we can read the next deployable target to attempt deployment operations on other
targets, or retry the same target if it is the only deployable one.
This is useful for campaigns that require an existing deployment to be present
(e.g., start, stop, upgrade, delete operations).

# Arguments

* campaign_id
* application_id

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `fetch_next_valid_target_with_application_deployed!`

Returns the next valid target whose device has a specific application deployed.

The next valid target is chosen with these criteria:
- Must be idle
- Must be online
- Must have the specified application deployed
- It must either not have been attempted before or it has to be the least
recently attempted target, in this order of preference.

This set of constraints guarantees that when we make an attempt on a
target that fails with a temporary error, given we update latest_attempt,
we can read the next deployable target to attempt deployment operations on other
targets, or retry the same target if it is the only deployable one.
This is useful for campaigns that require an existing deployment to be present
(e.g., start, stop, upgrade, delete operations).

Raises any errors instead of returning them

# Arguments

* campaign_id
* application_id

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `fetch_target`

Calls the read action on Edgehog.Campaigns.CampaignTarget.

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `fetch_target!`

Calls the read action on Edgehog.Campaigns.CampaignTarget.

Raises any errors instead of returning them

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `fetch_target_by_deployment`

Calls the read action on Edgehog.Campaigns.CampaignTarget.

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `fetch_target_by_deployment!`

Calls the read action on Edgehog.Campaigns.CampaignTarget.

Raises any errors instead of returning them

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `fetch_target_by_device_and_campaign`

Calls the read action on Edgehog.Campaigns.CampaignTarget.

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `fetch_target_by_device_and_campaign!`

Calls the read action on Edgehog.Campaigns.CampaignTarget.

Raises any errors instead of returning them

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `first`

> This function is deprecated. Use `Ash.first/3` instead.

# `first!`

> This function is deprecated. Use `Ash.first!/3` instead.

# `get`

> This function is deprecated. Use `Ash.get/3` instead.

# `get!`

> This function is deprecated. Use `Ash.get!/3` instead.

# `increase_target_retry_count`

Calls the increase_retry_count action on Edgehog.Campaigns.CampaignTarget.

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `increase_target_retry_count!`

Calls the increase_retry_count action on Edgehog.Campaigns.CampaignTarget.

Raises any errors instead of returning them

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `link_deployment`

Start a deployment towards this target.
It creates a Deployment and associates it with the target, sending all the
necessary requests to the device.
The target is marked as :in_progress.

# Arguments

* release

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `link_deployment!`

Start a deployment towards this target.
It creates a Deployment and associates it with the target, sending all the
necessary requests to the device.
The target is marked as :in_progress.

Raises any errors instead of returning them

# Arguments

* release

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `list`

> This function is deprecated. Use `Ash.list/3` instead.

# `list!`

> This function is deprecated. Use `Ash.list!/3` instead.

# `list_in_progress_targets`

Reads all the targets of a campaign that have `in_progress`
status. This is useful when resuming an campaign to know which
targets need to setup a retry timeout.

# Arguments

* campaign_id

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `list_in_progress_targets!`

Reads all the targets of a campaign that have `in_progress`
status. This is useful when resuming an campaign to know which
targets need to setup a retry timeout.

Raises any errors instead of returning them

# Arguments

* campaign_id

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `list_targets_with_pending_file_download_request`

Reads all the targets of a file download campaign that have a pending file
download request. This is useful when resuming a file download campaign to know which
targets need to setup a retry timeout.

# Arguments

* campaign_id

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `list_targets_with_pending_file_download_request!`

Reads all the targets of a file download campaign that have a pending file
download request. This is useful when resuming a file download campaign to know which
targets need to setup a retry timeout.

Raises any errors instead of returning them

# Arguments

* campaign_id

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `list_targets_with_pending_ota_operation`

Reads all the targets of an update campaign that have a pending OTA
operation. This is useful when resuming an update campaign to know which
targets need to setup a retry timeout.

# Arguments

* campaign_id

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `list_targets_with_pending_ota_operation!`

Reads all the targets of an update campaign that have a pending OTA
operation. This is useful when resuming an update campaign to know which
targets need to setup a retry timeout.

Raises any errors instead of returning them

# Arguments

* campaign_id

## Options

* `:page` - Pagination options, see `Ash.read/2` for more.

* `:load` (`t:term/0`) - A load statement to add onto the query

* `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

* `:lock` (`t:term/0`) - A lock statement to add onto the query

* `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.  
  The query goes through many potential changes during a request, potentially adding
  authorization filters, or replacing relationships for other data layers with their
  corresponding ids. This option can be used to get the true query that was sent to
  the data layer. The default value is `false`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

* `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
    a list of fields to fetch on a relationship, which allows for more
    optimized data-fetching.  
    See `Ash.Query.load/2`. The default value is `false`.

* `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. Valid values are :filter, :error The default value is `:filter`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

* `:not_found_error?` (`t:boolean/0`) - Whether or not to return or raise a `NotFound` error or to return `nil` when a get? action/interface is called.

* `:stream?` (`t:boolean/0`) - If true, a stream of the results will be returned The default value is `false`.

* `:stream_options` (`t:keyword/0`) - Options passed to `Ash.stream!`, if `stream?: true` is given

  * `:batch_size` (`t:integer/0`) - How many records to request in each query run. Defaults to the pagination limits on the resource, or 250.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

# `load`

> This function is deprecated. Use `Ash.load/3` instead.

# `load!`

> This function is deprecated. Use `Ash.load!/3` instead.

# `mark_campaign_failed`

Calls the mark_as_failed action on Edgehog.Campaigns.Campaign.

# Inputs

* completion_timestamp

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `mark_campaign_failed!`

Calls the mark_as_failed action on Edgehog.Campaigns.Campaign.

Raises any errors instead of returning them

# Inputs

* completion_timestamp

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `mark_campaign_in_progress`

Calls the mark_as_in_progress action on Edgehog.Campaigns.Campaign.

# Inputs

* start_timestamp

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `mark_campaign_in_progress!`

Calls the mark_as_in_progress action on Edgehog.Campaigns.Campaign.

Raises any errors instead of returning them

# Inputs

* start_timestamp

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `mark_campaign_paused`

Calls the mark_as_paused action on Edgehog.Campaigns.Campaign.

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `mark_campaign_paused!`

Calls the mark_as_paused action on Edgehog.Campaigns.Campaign.

Raises any errors instead of returning them

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `mark_campaign_successful`

Calls the mark_as_successful action on Edgehog.Campaigns.Campaign.

# Inputs

* completion_timestamp

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `mark_campaign_successful!`

Calls the mark_as_successful action on Edgehog.Campaigns.Campaign.

Raises any errors instead of returning them

# Inputs

* completion_timestamp

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `mark_target_as_failed`

Calls the mark_as_failed action on Edgehog.Campaigns.CampaignTarget.

# Inputs

* completion_timestamp

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `mark_target_as_failed!`

Calls the mark_as_failed action on Edgehog.Campaigns.CampaignTarget.

Raises any errors instead of returning them

# Inputs

* completion_timestamp

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `mark_target_as_in_progress`

Calls the mark_as_in_progress action on Edgehog.Campaigns.CampaignTarget.

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `mark_target_as_in_progress!`

Calls the mark_as_in_progress action on Edgehog.Campaigns.CampaignTarget.

Raises any errors instead of returning them

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `mark_target_as_successful`

Calls the mark_as_successful action on Edgehog.Campaigns.CampaignTarget.

# Inputs

* completion_timestamp

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `mark_target_as_successful!`

Calls the mark_as_successful action on Edgehog.Campaigns.CampaignTarget.

Raises any errors instead of returning them

# Inputs

* completion_timestamp

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `max`

> This function is deprecated. Use `Ash.max/3` instead.

# `max!`

> This function is deprecated. Use `Ash.max!/3` instead.

# `min`

> This function is deprecated. Use `Ash.min/3` instead.

# `min!`

> This function is deprecated. Use `Ash.min!/3` instead.

# `page`

> This function is deprecated. Use `Ash.page/2` instead.

# `page!`

> This function is deprecated. Use `Ash.page!/2` instead.

# `pause_campaign`

Calls the pause action on Edgehog.Campaigns.Campaign.

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `pause_campaign!`

Calls the pause action on Edgehog.Campaigns.Campaign.

Raises any errors instead of returning them

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `query_to_fetch_campaign`

Returns the query corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

# `query_to_fetch_next_valid_target`

Returns the query corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

# `query_to_fetch_next_valid_target_with_application_deployed`

Returns the query corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

# `query_to_fetch_target`

Returns the query corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

# `query_to_fetch_target_by_deployment`

Returns the query corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

# `query_to_fetch_target_by_device_and_campaign`

Returns the query corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

# `query_to_list_in_progress_targets`

Returns the query corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

# `query_to_list_targets_with_pending_file_download_request`

Returns the query corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

# `query_to_list_targets_with_pending_ota_operation`

Returns the query corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

# `read`

> This function is deprecated. Use `Ash.read/2` instead.

# `read!`

> This function is deprecated. Use `Ash.read!/2` instead.

# `read_one`

> This function is deprecated. Use `Ash.read_one/2` instead.

# `read_one!`

> This function is deprecated. Use `Ash.read_one!/2` instead.

# `reload`

> This function is deprecated. Use `Ash.reload/2` instead.

# `reload!`

> This function is deprecated. Use `Ash.reload!/2` instead.

# `resume_campaign`

Calls the resume action on Edgehog.Campaigns.Campaign.

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `resume_campaign!`

Calls the resume action on Edgehog.Campaigns.Campaign.

Raises any errors instead of returning them

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `run_action`

> This function is deprecated. Use `Ash.run_action/2` instead.

# `run_action!`

> This function is deprecated. Use `Ash.run_action/2` instead.

# `set_target_deployment`

Links an existing deployment to this target.
The target is marked as :in_progress.

# Arguments

* deployment_id

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `set_target_deployment!`

Links an existing deployment to this target.
The target is marked as :in_progress.

Raises any errors instead of returning them

# Arguments

* deployment_id

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `start_file_download`

Starts the file download for a target.
It creates a File Download Request, associates it with the campaign target, and
sends the download request to the device.
The campaign target is transitioned to the :in_progress status.

# Arguments

* file
* mechanism

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `start_file_download!`

Starts the file download for a target.
It creates a File Download Request, associates it with the campaign target, and
sends the download request to the device.
The campaign target is transitioned to the :in_progress status.

Raises any errors instead of returning them

# Arguments

* file
* mechanism

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `start_fw_upgrade`

Starts the OTA update for a target.
It creates an OTA Operation, associates it with the campaign target, and
sends the update request to the device.
The campaign target is transitioned to the :in_progress status.

# Arguments

* base_image

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `start_fw_upgrade!`

Starts the OTA update for a target.
It creates an OTA Operation, associates it with the campaign target, and
sends the update request to the device.
The campaign target is transitioned to the :in_progress status.

Raises any errors instead of returning them

# Arguments

* base_image

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `stream!`

> This function is deprecated. Use `Ash.stream!/2` instead.

# `sum`

> This function is deprecated. Use `Ash.sum/3` instead.

# `sum!`

> This function is deprecated. Use `Ash.sum!/3` instead.

# `update`

> This function is deprecated. Use `Ash.update/2` instead.

# `update!`

> This function is deprecated. Use `Ash.update!/2` instead.

# `update_target_latest_attempt`

Calls the update_latest_attempt action on Edgehog.Campaigns.CampaignTarget.

# Arguments

* latest_attempt - The timestamp of the latest attempt to deploy to the campaign target.

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `update_target_latest_attempt!`

Calls the update_latest_attempt action on Edgehog.Campaigns.CampaignTarget.

Raises any errors instead of returning them

# Arguments

* latest_attempt - The timestamp of the latest attempt to deploy to the campaign target.

## Options

* `:params` (`t:map/0`) - Parameters to supply, ignored if the input is a changeset, only used when an identifier is given.

* `:atomic_upgrade?` (`t:boolean/0`) - If true the action will be done atomically if it can (and is configured to do so), ignoring the in memory transformations and validations. You should not generally need to disable this. The default value is `true`.

* `:timeout` (`t:timeout/0`) - A positive integer, or `:infinity`. If none is provided, the timeout configured on the domain is used.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:action` (`t:term/0`) - The action to use, either an Action struct or the name of the action

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:context` (`t:map/0`) - Context to set on the query, changeset, or input

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:return_notifications?` (`t:boolean/0`) - Use this if you're running ash actions in your own transaction and you want to manually handle sending notifications.  
  If a transaction is ongoing, and this is false, notifications will be discarded, otherwise
  the return value is `{:ok, result, notifications}` (or `{:ok, notifications}`)  
  To send notifications later, use `Ash.Notifier.notify(notifications)`. It sends any notifications
  that can be sent, and returns the rest. The default value is `false`.

* `:rollback_on_error?` (`t:boolean/0`) - Whether or not to rollback the transaction on error, if the resource is in a transaction.  
  If the action has `transaction? false` this option has no effect. If an error is returned from the
  data layer and the resource is in a transaction, the transaction is always rolled back, regardless. The default value is `true`.

* `:notification_metadata` (`t:term/0`) - Metadata to be merged into the metadata field for all notifications sent from this operation. The default value is `%{}`.

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to add onto the changeset

* `:bulk_options` (`t:keyword/0`) - Options passed to `Ash.bulk_update`, if a query, list, or stream of inputs is provided.

  * `:atomic_update` (`t:map/0`) - A map of atomic updates to apply. See `Ash.Changeset.atomic_update/3` for more.

  * `:stream_batch_size` (`t:integer/0`) - Batch size to use if provided a query and the query must be streamed

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records if the `:stream` strategy is chosen. See the `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:authorize_query?` (`t:boolean/0`) - If a query is given, determines whether or not authorization is run on that query. The default value is `true`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:filter` (`t:term/0`) - A filter to apply to records. This is also applied to a stream of inputs.

  * `:strategy` - The strategy or strategies to enable. :stream is used in all cases if the data layer does not support atomics. The default value is `[:atomic]`.

  * `:transform_changeset` (function of arity 1) - A function that takes and returns a changeset, applied to each changeset after it is built but before validation. Used internally by managed relationships to set foreign keys and context.

  * `:allow_stream_with` - The 'worst' strategy allowed to be used to fetch records. See `Ash.stream!/2` docs for more. The default value is `:keyset`.

  * `:stream_with` - The specific strategy to use to fetch records. See `Ash.stream!/2` docs for more.

  * `:max_concurrency` (`t:non_neg_integer/0`) - The maximum number of processes allowed to be started for parallel loading of relationships and calculations. Defaults to `System.schedulers_online() * 2`

  * `:lock` (`t:term/0`) - A lock statement to add onto the query

  * `:return_query?` (`t:boolean/0`) - If `true`, the query that was ultimately used is returned as a third tuple element.

    The query goes through many potential changes during a request, potentially adding
    authorization filters, or replacing relationships for other data layers with their
    corresponding ids. This option can be used to get the true query that was sent to
    the data layer.

    The default value is `false`.

  * `:reuse_values?` (`t:boolean/0`) - Whether calculations are allowed to reuse values that have already been loaded, or must refetch them from the data layer. The default value is `false`.

  * `:strict?` (`t:boolean/0`) - If set to true, only specified attributes will be loaded when passing
      a list of fields to fetch on a relationship, which allows for more
      optimized data-fetching.

      See `Ash.Query.load/2`.

    The default value is `false`.

  * `:authorize_with` - If set to `:error`, instead of applying authorization filters as a filter, any records not matching the authorization filter will cause an error to be returned. The default value is `:filter`.

  * `:read_action` (`t:atom/0`) - The action to use when building the read query.

  * `:assume_casted?` (`t:boolean/0`) - Whether or not to cast attributes and arguments as input. This is an optimization for cases where the input is already casted and/or not in need of casting The default value is `false`.

  * `:select` (list of `t:atom/0`) - A select statement to apply to records. Ignored if `return_records?` is not true.

  * `:authorize_query_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_changeset_with` - If set to `:error`, instead of filtering unauthorized changes, unauthorized changes will raise an appropriate forbidden error. Uses `authorize_with` if not set.

  * `:authorize_with` - If set to `:error`, instead of filtering unauthorized query results, unauthorized query results will raise an appropriate forbidden error. The default value is `:filter`.

  * `:private_arguments` (`t:map/0`) - Private argument values to set on each changeset before validations and changes are run. The default value is `%{}`.

  * `:sorted?` (`t:boolean/0`) - Whether or not to sort results by their input position, in cases where `return_records?: true` was provided. The default value is `false`.

  * `:return_records?` (`t:boolean/0`) - Whether or not to return all of the records that were inserted. Defaults to false to account for large inserts. The default value is `false`.

  * `:return_errors?` (`t:boolean/0`) - Whether to return all errors that occur during the operation. Defaults to the value of `:bulk_actions_default_to_errors?` in your config, or `false` if not set. Returning all errors may be expensive for large inserts. The default value is `false`.

  * `:batch_size` (`t:pos_integer/0`) - The number of records to include in each batch. Defaults to the `default_limit`
    or `max_page_size` of the action, or 100.

  * `:return_stream?` (`t:boolean/0`) - If set to `true`, instead of an `Ash.BulkResult`, a mixed stream is returned.

    Potential elements:

    `{:notification, notification}` - if `return_notifications?` is set to `true`
    `{:ok, record}` - if `return_records?` is set to `true`
    `{:error, error}` - an error that occurred. May be changeset or an individual error.

    The default value is `false`.

  * `:return_nothing?` (`t:boolean/0`) - Mutes warnings about returning nothing.

    Only relevant if `return_stream?` is set to `true` and all other
    `return_*?` options are set to `false`.

    The default value is `false`.

  * `:stop_on_error?` (`t:boolean/0`) - If true, the first encountered error will stop the action and be returned. Otherwise, errors
    will be skipped. The default value is `false`.

  * `:notify?` (`t:boolean/0`) - Whether or not to generate any notifications. If this is set to `true` then the data layer must return
    the results from each batch. This may be intensive for large bulk actions.

    Notifications will be automatically sent unless `return_notifications?` is set to `true`.

    The default value is `false`.

  * `:transaction` - Whether or not to wrap the entire execution in a transaction, each batch, or not at all.

    Keep in mind:

    `before_transaction` and `after_transaction` hooks attached to changesets will have to be run
    *inside* the transaction if you choose `transaction: :all`.

    The default value is `:batch`.

  * `:max_concurrency` (`t:non_neg_integer/0`) - If set to a value greater than 0, up to that many tasks will be started to run batches asynchronously The default value is `0`.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.
