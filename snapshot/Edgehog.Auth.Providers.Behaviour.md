# `Edgehog.Auth.Providers.Behaviour`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.1/backend/lib/edgehog/auth/providers/behaviour.ex#L21)

Authz provider behavior.

# `context`

```elixir
@type context() :: term()
```

# `fga_access_tuple`

```elixir
@type fga_access_tuple() ::
  {subj :: String.t(), rel :: String.t(), type :: String.t()}
```

# `fga_tuple`

```elixir
@type fga_tuple() :: {subj :: String.t(), rel :: String.t(), obj :: String.t()}
```

# `obj_stream`

```elixir
@type obj_stream() :: term()
```

# `objects`

```elixir
@type objects() :: %{objects: [term()]}
```

# `users`

```elixir
@type users() :: %{users: [term()]}
```

# `check`

```elixir
@callback check(tuple :: fga_tuple(), context :: context()) ::
  {:ok, true} | {:ok, false} | {:error, term()}
```

A check call checks a tuple against the provider

- subj :: is some id of the person making the request, ideally a OpenID Connect UUID
- rel  :: is the requested access to the resource (object) in order to perform the action
- obj  :: is the resource the request is requiring access to

The context is also provided.

The check can return
- `{:ok, true}`     :: meaning that the subject has the right permission to access the resource
- `{:ok, false}`    :: meaning that the subject has not the right permission to access the resource
- `{:error, error}` :: meaning that there was some error in the request.

For successful returns the new `context` should be provided.

# `delete`

```elixir
@callback delete(tuple :: fga_tuple(), context :: context()) ::
  {:ok, term()} | {:error, term()}
```

Delete a tuple from the provider.

- tuple :: the fga tuple, composed of `subject`, `relationship` and `object`
- context :: the context from `init_context`

A delete can return
- `{:ok, result}`   :: if the delete was successful
- `{:error, error}` :: if some error was encountered while deleting

# `init_context`

```elixir
@callback init_context(args :: Keyword.t()) :: {:ok, context()} | {:error, term()}
```

The context initialization function. The context can carry useful information for subsequent actions.
For example: for OpenFGA's gRPC connections you might want to store here the channel, store_id and model_id.

# `list_objects`

```elixir
@callback list_objects(tuple :: fga_access_tuple(), context :: context()) ::
  {:ok, objects()} | {:ok, :all} | {:error, term()}
```

A list_objects call lists all objects of the selected type a user has access to.

- subj :: is some id of the person making the request, ideally a OpenID Connect UUID
- rel  :: is the requested access to the resource (object) in order to perform the action
- type :: is the type of resources we want to fetch

The context should also be provided.

NOTICE: This creates a list with all the objects! This might be very
inefficient and possibly stalls the request (e.g. 1mln devices), consider
using `stream_list_objects`

The call can return
- `{:ok, objects()}` :: meaning that the user has access to the %{objects: list()} list of objects of type `type`
- `{:error, error}`  :: meaning that there was some error in the request.

For successful returns the new `context` should be provided.

# `list_users`

```elixir
@callback list_users(tuple :: fga_access_tuple(), context :: context()) ::
  {:ok, users()} | {:ok, :all} | {:error, term()}
```

A list_users call lists all users of the selected type for the given object.

- subj :: is some id of the object for which the users are needed
- rel  :: is the requested access to the resource (object) the users should have
- type :: is the type of user resources we want to fetch

The context should also be provided.

NOTICE: Unlike it's opposite counterpart (`list_objects`), this does not provide a streamed version of the same function

The call can return
- `{:ok, users()}` :: meaning that the object has access to the %{objects: list()} list of objects of type `type`
- `{:error, error}`  :: meaning that there was some error in the request.

For successful returns the new `context` should be provided.

# `stream_list_objects`

```elixir
@callback stream_list_objects(tuple :: fga_access_tuple(), context :: context()) ::
  {:ok, obj_stream()} | {:ok, :all} | {:error, term()}
```

A stream_list_objects call streams all objects of the selected type a user has access to.

- subj :: is some id of the person making the request, ideally a OpenID Connect UUID
- rel  :: is the requested access to the resource (object) in order to perform the action
- type :: is the type of resources we want to fetch

The context should also be provided.

The call can return
- `{:ok, stream(objects())}` :: meaning that the user has access to the %{objects: list()} list of objects of type `type`
- `{:error, error}`          :: meaning that there was some error in the request.

For successful returns the new `context` should be provided.

# `write`

```elixir
@callback write(tuple :: fga_tuple(), context :: context()) ::
  {:ok, term()} | {:error, term()}
```

Writes a tuple to the provider.

- tuple :: the fga tuple, composed of `subject`, `relationship` and `object`
- context :: the context from `init_context`

A write can return
- `{:ok, result}`   :: if the write was successful
- `{:error, error}` :: if some error was encountered while writing

