# `Edgehog.Auth.Providers.Behaviour`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/auth/providers/behaviour.ex#L21)

Authz provider behavior.

# `context`

```elixir
@type context() :: term()
```

# `fga_tuple`

```elixir
@type fga_tuple() :: {subj :: String.t(), rel :: String.t(), obj :: String.t()}
```

# `check`

```elixir
@callback check(tuple :: fga_tuple(), context :: context()) ::
  :ok | :notok | {:error, term()}
```

A check call checks a tuple against the provider

- subj :: is some id of the person making the request, ideally a OpenID Connect UUID
- rel  :: is the requested access to the resource (object) in order to perform the action
- obj  :: is the resource the request is requiring access to

The context is also provided.

The check can return
- {:ok, context()}    :: meaning that the subject has the right permission to access the resource
- {:notok, context()} :: meaning that the subject has not the right permission to access the resource
- {:error, error}     :: meaning that there was some error in the request.

For successful returns the new `context` should be provided.

# `init_context`

```elixir
@callback init_context(args :: Keyword.t()) :: {:ok, context()} | {:error, term()}
```

The context initialization function. The context can carry useful information for subsequent actions.
For example: for OpenFGA's gRPC connections you might want to store here the channel, store_id and model_id.

