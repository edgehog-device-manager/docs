# `Edgehog.Files`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/files/files.ex#L21)

The `Edgehog.Files` domain, which includes resources and logic related to file management.

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

# `can_fetch_file_download_request`

Runs authorization checks for `Edgehog.Files.FileDownloadRequest.read`

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

# `can_fetch_file_download_request?`

Runs authorization checks for `Edgehog.Files.FileDownloadRequest.read`, returning a boolean.

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

# `can_fetch_file_upload_request`

Runs authorization checks for `Edgehog.Files.FileUploadRequest.read`

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

# `can_fetch_file_upload_request?`

Runs authorization checks for `Edgehog.Files.FileUploadRequest.read`, returning a boolean.

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

# `can_send_file_download_request`

Runs authorization checks for `Edgehog.Files.FileDownloadRequest.send_file_download_request`

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

# `can_send_file_download_request?`

Runs authorization checks for `Edgehog.Files.FileDownloadRequest.send_file_download_request`, returning a boolean.

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

# `can_send_file_upload_request`

Runs authorization checks for `Edgehog.Files.FileUploadRequest.send_file_upload_request`

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

# `can_send_file_upload_request?`

Runs authorization checks for `Edgehog.Files.FileUploadRequest.send_file_upload_request`, returning a boolean.

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

# `can_set_file_download_progress`

Runs authorization checks for `Edgehog.Files.FileDownloadRequest.set_progress`

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

# `can_set_file_download_progress?`

Runs authorization checks for `Edgehog.Files.FileDownloadRequest.set_progress`, returning a boolean.

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

# `can_set_file_download_response`

Runs authorization checks for `Edgehog.Files.FileDownloadRequest.set_response`

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

# `can_set_file_download_response?`

Runs authorization checks for `Edgehog.Files.FileDownloadRequest.set_response`, returning a boolean.

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

# `can_set_file_download_status`

Runs authorization checks for `Edgehog.Files.FileDownloadRequest.set_status`

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

# `can_set_file_download_status?`

Runs authorization checks for `Edgehog.Files.FileDownloadRequest.set_status`, returning a boolean.

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

# `can_set_file_upload_progress`

Runs authorization checks for `Edgehog.Files.FileUploadRequest.set_file_upload_progress`

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

# `can_set_file_upload_progress?`

Runs authorization checks for `Edgehog.Files.FileUploadRequest.set_file_upload_progress`, returning a boolean.

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

# `can_set_file_upload_request_status`

Runs authorization checks for `Edgehog.Files.FileUploadRequest.update_status`

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

# `can_set_file_upload_request_status?`

Runs authorization checks for `Edgehog.Files.FileUploadRequest.update_status`, returning a boolean.

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

# `can_set_file_upload_response`

Runs authorization checks for `Edgehog.Files.FileUploadRequest.set_file_upload_response`

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

# `can_set_file_upload_response?`

Runs authorization checks for `Edgehog.Files.FileUploadRequest.set_file_upload_response`, returning a boolean.

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

# `can_set_path_on_device`

Runs authorization checks for `Edgehog.Files.FileDownloadRequest.set_path_on_device`

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

# `can_set_path_on_device?`

Runs authorization checks for `Edgehog.Files.FileDownloadRequest.set_path_on_device`, returning a boolean.

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

# `can_set_size_bytes`

Runs authorization checks for `Edgehog.Files.FileDownloadRequest.set_size_bytes`

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

# `can_set_size_bytes?`

Runs authorization checks for `Edgehog.Files.FileDownloadRequest.set_size_bytes`, returning a boolean.

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

# `changeset_to_set_file_download_progress`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_set_file_download_response`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_set_file_download_status`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_set_file_upload_progress`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_set_file_upload_request_status`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_set_file_upload_response`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_set_path_on_device`

Returns the changeset corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

# `changeset_to_set_size_bytes`

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

# `fetch_file_download_request`

Calls the read action on Edgehog.Files.FileDownloadRequest.

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

# `fetch_file_download_request!`

Calls the read action on Edgehog.Files.FileDownloadRequest.

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

# `fetch_file_upload_request`

Calls the read action on Edgehog.Files.FileUploadRequest.

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

# `fetch_file_upload_request!`

Calls the read action on Edgehog.Files.FileUploadRequest.

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

# `input_to_send_file_download_request`

Returns the input corresponding to the action.

## Options

* `:actor` (`t:term/0`) - The actor for handling `^actor/1` templates, supplied to calculation context.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Will overwrite any actor, tenant or context provided. See `Ash.Context` for more.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant, supplied to calculation context.

* `:authorize?` (`t:boolean/0`) - Whether or not the request should be authorized.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer, provided to the calculation context.

# `input_to_send_file_upload_request`

Returns the input corresponding to the action.

## Options

* `:actor` (`t:term/0`) - The actor for handling `^actor/1` templates, supplied to calculation context.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Will overwrite any actor, tenant or context provided. See `Ash.Context` for more.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant, supplied to calculation context.

* `:authorize?` (`t:boolean/0`) - Whether or not the request should be authorized.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer, provided to the calculation context.

# `list`

> This function is deprecated. Use `Ash.list/3` instead.

# `list!`

> This function is deprecated. Use `Ash.list!/3` instead.

# `load`

> This function is deprecated. Use `Ash.load/3` instead.

# `load!`

> This function is deprecated. Use `Ash.load!/3` instead.

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

# `query_to_fetch_file_download_request`

Returns the query corresponding to the action.

## Options

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer that implements the `Ash.Tracer` behaviour. See that module for more.

* `:authorize?` - If an actor option is provided (even if it is `nil`), authorization happens automatically. If not, this flag can be used to authorize with no user.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - A tenant to set on the query or changeset

* `:actor` (`t:term/0`) - If an actor is provided, it will be used in conjunction with the authorizers of a resource to authorize access

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol, for passing around actor/tenant/context in a single value. See `Ash.Scope.ToOpts` for more.

* `:query` - A query to seed the action with.

# `query_to_fetch_file_upload_request`

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

# `run_action`

> This function is deprecated. Use `Ash.run_action/2` instead.

# `run_action!`

> This function is deprecated. Use `Ash.run_action/2` instead.

# `send_file_download_request`

Calls the send_file_download_request action on Edgehog.Files.FileDownloadRequest.

# Arguments

* file_download_request

## Options

* `:actor` (`t:term/0`) - The actor for handling `^actor/1` templates, supplied to calculation context.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Will overwrite any actor, tenant or context provided. See `Ash.Context` for more.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant, supplied to calculation context.

* `:authorize?` (`t:boolean/0`) - Whether or not the request should be authorized.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer, provided to the calculation context.

* `:context` (`t:map/0`) - Context to set on the action input

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to apply on the resulting records after the action is invoked.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `send_file_download_request!`

Calls the send_file_download_request action on Edgehog.Files.FileDownloadRequest.

Raises any errors instead of returning them

# Arguments

* file_download_request

## Options

* `:actor` (`t:term/0`) - The actor for handling `^actor/1` templates, supplied to calculation context.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Will overwrite any actor, tenant or context provided. See `Ash.Context` for more.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant, supplied to calculation context.

* `:authorize?` (`t:boolean/0`) - Whether or not the request should be authorized.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer, provided to the calculation context.

* `:context` (`t:map/0`) - Context to set on the action input

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to apply on the resulting records after the action is invoked.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `send_file_upload_request`

Calls the send_file_upload_request action on Edgehog.Files.FileUploadRequest.

# Arguments

* file_upload_request

## Options

* `:actor` (`t:term/0`) - The actor for handling `^actor/1` templates, supplied to calculation context.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Will overwrite any actor, tenant or context provided. See `Ash.Context` for more.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant, supplied to calculation context.

* `:authorize?` (`t:boolean/0`) - Whether or not the request should be authorized.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer, provided to the calculation context.

* `:context` (`t:map/0`) - Context to set on the action input

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to apply on the resulting records after the action is invoked.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `send_file_upload_request!`

Calls the send_file_upload_request action on Edgehog.Files.FileUploadRequest.

Raises any errors instead of returning them

# Arguments

* file_upload_request

## Options

* `:actor` (`t:term/0`) - The actor for handling `^actor/1` templates, supplied to calculation context.

* `:scope` (`t:term/0`) - A value that implements the `Ash.Scope.ToOpts` protocol. Will overwrite any actor, tenant or context provided. See `Ash.Context` for more.

* `:tenant` (value that implements the `Ash.ToTenant` protocol) - The tenant, supplied to calculation context.

* `:authorize?` (`t:boolean/0`) - Whether or not the request should be authorized.

* `:tracer` (one or a list of module that adopts `Ash.Tracer`) - A tracer, provided to the calculation context.

* `:context` (`t:map/0`) - Context to set on the action input

* `:skip_unknown_inputs` - A list of inputs that, if provided, will be ignored if they are not recognized by the action. Use `:*` to indicate all unknown keys.

* `:load` (`t:term/0`) - A load statement to apply on the resulting records after the action is invoked.

* `:private_arguments` (`t:map/0`) - Private argument values to set before validations and changes. The default value is `%{}`.

# `set_file_download_progress`

Calls the set_progress action on Edgehog.Files.FileDownloadRequest.

# Inputs

* status - The status of the file download (e.g., 'pending', 'sent', 'in_progress', 'completed', 'failed').
* progress_percentage - The progress of the file download as a percentage (0-100).

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

# `set_file_download_progress!`

Calls the set_progress action on Edgehog.Files.FileDownloadRequest.

Raises any errors instead of returning them

# Inputs

* status - The status of the file download (e.g., 'pending', 'sent', 'in_progress', 'completed', 'failed').
* progress_percentage - The progress of the file download as a percentage (0-100).

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

# `set_file_download_response`

Calls the set_response action on Edgehog.Files.FileDownloadRequest.

# Inputs

* status - The status of the file download (e.g., 'pending', 'sent', 'in_progress', 'completed', 'failed').
* response_code - A 0 code is a success, errors are POSIX error numbers.
* response_message - Optional message for the response sent by the device.
* progress_percentage - The progress of the file download as a percentage (0-100).

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

# `set_file_download_response!`

Calls the set_response action on Edgehog.Files.FileDownloadRequest.

Raises any errors instead of returning them

# Inputs

* status - The status of the file download (e.g., 'pending', 'sent', 'in_progress', 'completed', 'failed').
* response_code - A 0 code is a success, errors are POSIX error numbers.
* response_message - Optional message for the response sent by the device.
* progress_percentage - The progress of the file download as a percentage (0-100).

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

# `set_file_download_status`

Calls the set_status action on Edgehog.Files.FileDownloadRequest.

# Inputs

* status - The status of the file download (e.g., 'pending', 'sent', 'in_progress', 'completed', 'failed').

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

# `set_file_download_status!`

Calls the set_status action on Edgehog.Files.FileDownloadRequest.

Raises any errors instead of returning them

# Inputs

* status - The status of the file download (e.g., 'pending', 'sent', 'in_progress', 'completed', 'failed').

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

# `set_file_upload_progress`

Calls the set_file_upload_progress action on Edgehog.Files.FileUploadRequest.

# Inputs

* status
* progress_percentage

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

# `set_file_upload_progress!`

Calls the set_file_upload_progress action on Edgehog.Files.FileUploadRequest.

Raises any errors instead of returning them

# Inputs

* status
* progress_percentage

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

# `set_file_upload_request_status`

Calls the update_status action on Edgehog.Files.FileUploadRequest.

# Arguments

* status

# Inputs

* response_code
* response_message
* progress_percentage

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

# `set_file_upload_request_status!`

Calls the update_status action on Edgehog.Files.FileUploadRequest.

Raises any errors instead of returning them

# Arguments

* status

# Inputs

* response_code
* response_message
* progress_percentage

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

# `set_file_upload_response`

Calls the set_file_upload_response action on Edgehog.Files.FileUploadRequest.

# Inputs

* status
* response_code
* response_message

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

# `set_file_upload_response!`

Calls the set_file_upload_response action on Edgehog.Files.FileUploadRequest.

Raises any errors instead of returning them

# Inputs

* status
* response_code
* response_message

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

# `set_path_on_device`

Calls the set_path_on_device action on Edgehog.Files.FileDownloadRequest.

# Arguments

* path_on_device

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

# `set_path_on_device!`

Calls the set_path_on_device action on Edgehog.Files.FileDownloadRequest.

Raises any errors instead of returning them

# Arguments

* path_on_device

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

# `set_size_bytes`

Calls the set_size_bytes action on Edgehog.Files.FileDownloadRequest.

# Arguments

* decompressed_file_size_bytes

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

# `set_size_bytes!`

Calls the set_size_bytes action on Edgehog.Files.FileDownloadRequest.

Raises any errors instead of returning them

# Arguments

* decompressed_file_size_bytes

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

