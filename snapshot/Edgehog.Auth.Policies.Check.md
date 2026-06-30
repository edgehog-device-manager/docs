# `Edgehog.Auth.Policies.Check`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.1/backend/lib/edgehog/auth/policies/check.ex#L21)

An `Ash.Policy.SimpleCheck`, checking the user `subj` has access to the object of type `obj`.
You can optionally pass the `obj_id` attribute name.

To use it in a policy:
```elixir
authorize_if {Edgehog.Auth.Policies.Check, rel: :can_view, obj: :realm, obj_id: :name}
```

# `eager_evaluate?`

# `init`

# `prefer_expanded_description?`

# `requires_original_data?`

# `strict_check`

# `type`

