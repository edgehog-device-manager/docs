# `EdgehogWeb.AdminAPI.Auth.Token.Plug`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog_web/admin_api/auth/token.ex#L23)

# `authenticated?`

# `clear_remember_me`

# `current_claims`

# `current_resource`

# `current_token`

# `implementation`

```elixir
@spec implementation() :: EdgehogWeb.AdminAPI.Auth.Token
```

# `put_current_claims`

# `put_current_resource`

# `put_current_token`

# `put_session_token`

# `remember_me`

# `remember_me_from_token`

```elixir
@spec remember_me_from_token(
  Plug.Conn.t(),
  Guardian.Token.token(),
  Guardian.Token.claims(),
  Guardian.options()
) :: Plug.Conn.t()
```

# `sign_in`

# `sign_out`

