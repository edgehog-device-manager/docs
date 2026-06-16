# `Edgehog.Auth.Policies.Filter`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.0/backend/lib/edgehog/auth/policies/filter.ex#L21)

An `Ash.Policy.FilterCheck`, filtering the object of type `obj` available to the user `subj`.

To use it in a policy:
```elixir
authorize_if {Edgehog.Auth.Policies.Filter, rel: :can_view, obj: :device}
```

# `auto_filter`

# `auto_filter_not`

# `check`

# `eager_evaluate?`

# `expand_description`

# `init`

# `prefer_expanded_description?`

# `reject`

# `requires_original_data?`

# `strict_check`

# `strict_check_context`

# `type`

