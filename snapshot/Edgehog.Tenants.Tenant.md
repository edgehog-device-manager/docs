# `Edgehog.Tenants.Tenant`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.0/backend/lib/edgehog/tenants/tenant/tenant.ex#L21)

Tenant resource schema and operations.

# `record`

```elixir
@type record() :: Ash.Resource.record()
```

# `t`

```elixir
@type t() :: %Edgehog.Tenants.Tenant{
  __lateral_join_source__: term(),
  __meta__: term(),
  __metadata__: term(),
  __order__: term(),
  aggregates: term(),
  calculations: term(),
  default_locale: term(),
  inserted_at: term(),
  name: term(),
  public_key: term(),
  realm: term(),
  slug: term(),
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

# `json_api_match_route`

# `primary_key_matches?`

