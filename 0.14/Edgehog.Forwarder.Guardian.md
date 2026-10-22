# `Edgehog.Forwarder.Guardian`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.2/backend/lib/edgehog/forwarder/guardian.ex#L21)

Auth layer to handle connections to the device forwarder.

# `after_encode_and_sign`

# `after_sign_in`

# `before_sign_out`

# `build_claims`

# `config`

```elixir
@spec config() :: Keyword.t()
```

Fetches the configuration for this module.

# `config`

```elixir
@spec config(atom() | String.t(), any()) :: any()
```

Returns a resolved value of the configuration found at a key.

See `Guardian.Config.resolve_value/1`.

# `decode_and_verify`

```elixir
@spec decode_and_verify(
  Guardian.Token.token(),
  Guardian.Token.claims(),
  Guardian.options()
) ::
  {:ok, Guardian.Token.claims()} | {:error, any()}
```

Decodes and verifies a token using the configuration on the implementation
module.

See `Guardian.decode_and_verify/4`.

# `default_token_type`

```elixir
@spec default_token_type() :: String.t()
```

The default type of token for this module.

# `encode_and_sign`

```elixir
@spec encode_and_sign(any(), Guardian.Token.claims(), Guardian.options()) ::
  {:ok, Guardian.Token.token(), Guardian.Token.claims()} | {:error, any()}
```

Encodes the claims.

See `Guardian.encode_and_sign/4` for more information.

# `exchange`

```elixir
@spec exchange(
  token :: Guardian.Token.token(),
  from_type :: String.t() | [String.t(), ...],
  to_type :: String.t(),
  options :: Guardian.options()
) ::
  {:ok, {Guardian.Token.token(), Guardian.Token.claims()},
   {Guardian.Token.token(), Guardian.Token.claims()}}
  | {:error, any()}
```

Exchanges a token of one type for another.

See `Guardian.exchange` for more information.

# `on_exchange`

# `on_refresh`

# `on_revoke`

# `on_verify`

# `peek`

```elixir
@spec peek(String.t()) :: map()
```

Provides the content of the token but without verification
of either the claims or the signature.

Claims will be present at the `:claims` key.

See `Guardian.peek/2` for more information.

# `refresh`

```elixir
@spec refresh(Guardian.Token.token(), Guardian.options()) ::
  {:ok, {Guardian.Token.token(), Guardian.Token.claims()},
   {Guardian.Token.token(), Guardian.Token.claims()}}
  | {:error, any()}
```

Refresh a token.

See `Guardian.refresh` for more information.

# `resource_from_claims`

# `resource_from_token`

```elixir
@spec resource_from_token(
  token :: Guardian.Token.token(),
  claims_to_check :: Guardian.Token.claims() | nil,
  opts :: Guardian.options()
) :: {:ok, Guardian.Token.resource(), Guardian.Token.claims()} | {:error, any()}
```

Fetch the resource and claims directly from a token.

See `Guardian.resource_from_token` for more information.

# `revoke`

```elixir
@spec revoke(Guardian.Token.token(), Guardian.options()) ::
  {:ok, Guardian.Token.claims()} | {:error, any()}
```

Revoke a token.

See `Guardian.revoke` for more information.

# `sliding_cookie`

```elixir
@spec sliding_cookie(
  current_claims :: Guardian.Token.claims(),
  current_resource :: Guardian.Token.resource(),
  options :: Guardian.options()
) :: {:ok, new_claims :: Guardian.Token.claims()} | {:error, any()}
```

If Guardian.Plug.SlidingCookie is used, this callback will be invoked to
return the new claims, or an error (which will mean the cookie will not
be refreshed).

# `subject_for_token`

# `verify_claims`

