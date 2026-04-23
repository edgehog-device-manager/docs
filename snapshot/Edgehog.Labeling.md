# `Edgehog.Labeling`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/labeling/labeling.ex#L19)

The Labeling context, containing all functionalities regarding tags and attributes assignment

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

# `first`

> This function is deprecated. Use `Ash.first/3` instead.

# `first!`

> This function is deprecated. Use `Ash.first!/3` instead.

# `get`

> This function is deprecated. Use `Ash.get/3` instead.

# `get!`

> This function is deprecated. Use `Ash.get!/3` instead.

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

