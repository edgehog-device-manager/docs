# `Edgehog.Tenants.Reconciler.Context`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.1/backend/lib/edgehog/tenants/reconciler/context.ex#L21)

Helper function for tenant reconciliation.

The functions below let core modules interact with the context: adding,
changing keys, adding errors, checking the presence of errors, etc.

The context is a map. keys can be arbitrarily added and fetched, however, some keys are present by default:

- tenant                  :: the given tenant, for which we're building the context
- realm_management_client :: the realm management client to interact with astarte
- astarte_version         :: the astarte version
- errors                  :: a Keyword list of errors, scoped per reconciler section (delivery policies, triggers, interfaces)

# `add_context`

Adds a key to the context.

Example:

```elixir
add_context(context, delivery_policies_compatible: false)
```

# `add_error`

Adds an error to the context, in the corresponding section

Sections are handled as keys in a keyword list (the errors in the context):

```elixir
%{
  errors: [
    delivery_policies: [
      error1,
      error2,
      error3,
      ...
    ]
  ]
}
```

# `build`

Builds a context, given a tenant.

This will only provide the initial context. A context is a map. Keys can be added as you go, but some keys are provided here:

- tenant                  :: the given tenant, for which we're building the context
- realm_management_client :: the realm management client to interact with astarte
- astarte_version         :: the astarte version
- errors                  :: a Keyword list of errors, scoped per reconciler section (delivery policies, triggers, interfaces). The list is empty by default

```elixir
%{
  tenant: tenant,
  rm_client: realm_management_client,
  astarte_version: astarte_version,
  errors: []
}
```

You might want to match on the following possible return values

- `{:ok, context}`                       :: The context was successfully iniyialized.
- `{:error, :missing_rm_client}`         :: The realm management client was not correctly initialized. Possibly as misconfiguration of the astarte realm.
- `{:error, :invalid_tenant}`            :: The provided tenant was not valid.
- `{:error, %Astarte.Client.APIError{}}` :: There was a communication error with astarte.

# `errors?`

Checks whether there are errors or a specific section has errors.

## Examples:

```elixir
> context = %{errors: []}
%{errors: []}

> Context.errors?(context)
false
```

```elixir
> context = %{errors: [sec_1: [:some_error]]}
%{errors: [sec_1: [:some_error]]}

> Context.errors?(context, :sec_1)
true

> Context.errors?(context, :sec_2)
false

> Context.errors?(context)
true
```

# `get_context`

Retrieves a key from the context, defaulting to a default value if not present:

Example: 

```elixir
get_context(context, :delivery_policies_compatible, true)
```

