# `Edgehog.Actors.Actor`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/actors/actor.ex#L21)

Edgheog Actors.
This module represents an actor performing a call trough the GraphQL APIs.
It implements the ID Token from the OpenID Connect spec.

# `t`

```elixir
@type t() :: %Edgehog.Actors.Actor{
  __lateral_join_source__: term(),
  __meta__: term(),
  __metadata__: term(),
  __order__: term(),
  aggregates: term(),
  aud: term(),
  auth_time: term(),
  calculations: term(),
  claims: term(),
  email: term(),
  exp: term(),
  family_name: term(),
  given_name: term(),
  iat: term(),
  preferred_username: term(),
  sub: term()
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

