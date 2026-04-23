# `Edgehog.Config`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/config.ex#L21)

This module handles the configuration of Edgehog

# `admin_jwk`

```elixir
@spec admin_jwk(Skogsra.Env.namespace()) ::
  {:ok, nil | Edgehog.Config.JWTPublicKeyPEMType.t()} | {:error, binary()}
```

The Admin API JWT public key.

Calling `Edgehog.Config.admin_jwk()` will ensure the following:

- Binding order: [:system, :config]
- OS environment variable: "ADMIN_JWT_PUBLIC_KEY_PATH"
- Type: Edgehog.Config.JWTPublicKeyPEMType
- Default: nil
- Required: false
- Cached: true

# `admin_jwk!`

```elixir
@spec admin_jwk!(Skogsra.Env.namespace()) ::
  (nil | Edgehog.Config.JWTPublicKeyPEMType.t()) | no_return()
```

The Admin API JWT public key.

Bang version of `Edgehog.Config.admin_jwk/0` (fails on error). Optionally,
receives the `namespace` for the variable.

# `authz_config!`

```elixir
@spec authz_config!() :: Keyword.t()
```

Returns the FGA provider configuration.

# `authz_provider`

```elixir
@spec authz_provider(Skogsra.Env.namespace()) ::
  {:ok, Edgehog.Config.AuthzProvider.t()} | {:error, binary()}
```

The preferred fine grained authorization provider.
Possible values are: none

Calling `Edgehog.Config.authz_provider()` will ensure the following:

- Binding order: [:system, :config]
- OS environment variable: "AUTHZ_PROVIDER"
- Type: Edgehog.Config.AuthzProvider
- Default: Edgehog.Auth.Providers.None
- Required: false
- Cached: true

# `authz_provider!`

```elixir
@spec authz_provider!(Skogsra.Env.namespace()) ::
  Edgehog.Config.AuthzProvider.t() | no_return()
```

The preferred fine grained authorization provider.
Possible values are: none

Bang version of `Edgehog.Config.authz_provider/0` (fails on error). Optionally,
receives the `namespace` for the variable.

# `database_enable_ssl`

```elixir
@spec database_enable_ssl(Skogsra.Env.namespace()) ::
  {:ok, boolean()} | {:error, binary()}
```

Whether edgehog should use a tls connection with the database or not.

Calling `Edgehog.Config.database_enable_ssl()` will ensure the following:

- Binding order: [:system, :config]
- OS environment variable: "DATABASE_ENABLE_SSL"
- Type: :boolean
- Default: false
- Required: false
- Cached: true

# `database_enable_ssl!`

```elixir
@spec database_enable_ssl!(Skogsra.Env.namespace()) :: boolean() | no_return()
```

Whether edgehog should use a tls connection with the database or not.

Bang version of `Edgehog.Config.database_enable_ssl/0` (fails on error). Optionally,
receives the `namespace` for the variable.

# `database_enable_ssl?`

```elixir
@spec database_enable_ssl?() :: boolean()
```

Returns true if edgehog should use an ssl connection with the database.

# `database_ssl_cacertfile`

```elixir
@spec database_ssl_cacertfile(Skogsra.Env.namespace()) ::
  {:ok, binary()} | {:error, binary()}
```

The certificate file to use to verify the ssl connection with the database.

Calling `Edgehog.Config.database_ssl_cacertfile()` will ensure the following:

- Binding order: [:system, :config]
- OS environment variable: "DATABASE_SSL_CACERTFILE"
- Type: :binary
- Default: ""
- Required: false
- Cached: true

# `database_ssl_cacertfile!`

```elixir
@spec database_ssl_cacertfile!(Skogsra.Env.namespace()) :: binary() | no_return()
```

The certificate file to use to verify the ssl connection with the database.

Bang version of `Edgehog.Config.database_ssl_cacertfile/0` (fails on error). Optionally,
receives the `namespace` for the variable.

# `database_ssl_config`

```elixir
@spec database_ssl_config() :: false | [term()]
```

Returns the database configuration for the database connection.

# `database_ssl_config_opts`

```elixir
@spec database_ssl_config_opts() :: [term()]
```

Returns the Ecto configuration for the ssl connection to the database.

# `database_ssl_verify`

```elixir
@spec database_ssl_verify(Skogsra.Env.namespace()) ::
  {:ok, boolean()} | {:error, binary()}
```

Whether to verify the ssl connection with the database or not.

Calling `Edgehog.Config.database_ssl_verify()` will ensure the following:

- Binding order: [:system, :config]
- OS environment variable: "DATABASE_SSL_VERIFY"
- Type: :boolean
- Default: false
- Required: false
- Cached: true

# `database_ssl_verify!`

```elixir
@spec database_ssl_verify!(Skogsra.Env.namespace()) :: boolean() | no_return()
```

Whether to verify the ssl connection with the database or not.

Bang version of `Edgehog.Config.database_ssl_verify/0` (fails on error). Optionally,
receives the `namespace` for the variable.

# `database_ssl_verify?`

```elixir
@spec database_ssl_verify?() :: boolean()
```

Returns whether to verify the ssl connection with he database or not.

# `database_use_os_certs`

```elixir
@spec database_use_os_certs(Skogsra.Env.namespace()) ::
  {:ok, boolean()} | {:error, binary()}
```

Whether to use the os certificates to communicate with the database over ssl.

Calling `Edgehog.Config.database_use_os_certs()` will ensure the following:

- Binding order: [:system, :config]
- OS environment variable: "DATABASE_USE_OS_CERTS"
- Type: :boolean
- Default: false
- Required: false
- Cached: true

# `database_use_os_certs!`

```elixir
@spec database_use_os_certs!(Skogsra.Env.namespace()) :: boolean() | no_return()
```

Whether to use the os certificates to communicate with the database over ssl.

Bang version of `Edgehog.Config.database_use_os_certs/0` (fails on error). Optionally,
receives the `namespace` for the variable.

# `database_use_os_certs?`

```elixir
@spec database_use_os_certs?() :: boolean()
```

Returns true if edgehog should use the operative system certificates.

# `geocoding_providers!`

```elixir
@spec geocoding_providers!() :: [atom()]
```

Returns the list of geocoding modules to use.

# `geolocation_providers!`

```elixir
@spec geolocation_providers!() :: [atom()]
```

Returns the list of geolocation modules to use.

# `google_geocoding_api_key`

```elixir
@spec google_geocoding_api_key(Skogsra.Env.namespace()) ::
  {:ok, nil | binary()} | {:error, binary()}
```

The API key for the Google geocoding provider.

Calling `Edgehog.Config.google_geocoding_api_key()` will ensure the following:

- Binding order: [:system, :config]
- OS environment variable: "GOOGLE_GEOCODING_API_KEY"
- Type: :binary
- Default: nil
- Required: false
- Cached: true

# `google_geocoding_api_key!`

```elixir
@spec google_geocoding_api_key!(Skogsra.Env.namespace()) ::
  (nil | binary()) | no_return()
```

The API key for the Google geocoding provider.

Bang version of `Edgehog.Config.google_geocoding_api_key/0` (fails on error). Optionally,
receives the `namespace` for the variable.

# `google_geolocation_api_key`

```elixir
@spec google_geolocation_api_key(Skogsra.Env.namespace()) ::
  {:ok, nil | binary()} | {:error, binary()}
```

The API key for the Google geolocation provider.

Calling `Edgehog.Config.google_geolocation_api_key()` will ensure the following:

- Binding order: [:system, :config]
- OS environment variable: "GOOGLE_GEOLOCATION_API_KEY"
- Type: :binary
- Default: nil
- Required: false
- Cached: true

# `google_geolocation_api_key!`

```elixir
@spec google_geolocation_api_key!(Skogsra.Env.namespace()) ::
  (nil | binary()) | no_return()
```

The API key for the Google geolocation provider.

Bang version of `Edgehog.Config.google_geolocation_api_key/0` (fails on error). Optionally,
receives the `namespace` for the variable.

# `ipbase_api_key`

```elixir
@spec ipbase_api_key(Skogsra.Env.namespace()) ::
  {:ok, nil | binary()} | {:error, binary()}
```

The API key for the ipbase.com geolocation provider.

Calling `Edgehog.Config.ipbase_api_key()` will ensure the following:

- Binding order: [:system, :config]
- OS environment variable: "IPBASE_API_KEY"
- Type: :binary
- Default: nil
- Required: false
- Cached: true

# `ipbase_api_key!`

```elixir
@spec ipbase_api_key!(Skogsra.Env.namespace()) :: (nil | binary()) | no_return()
```

The API key for the ipbase.com geolocation provider.

Bang version of `Edgehog.Config.ipbase_api_key/0` (fails on error). Optionally,
receives the `namespace` for the variable.

# `preferred_geocoding_providers`

```elixir
@spec preferred_geocoding_providers(Skogsra.Env.namespace()) ::
  {:ok, Edgehog.Config.GeocodingProviders.t()} | {:error, binary()}
```

A comma separated list of preferred geocoding providers.
Possible values are: google

Calling `Edgehog.Config.preferred_geocoding_providers()` will ensure the following:

- Binding order: [:system, :config]
- OS environment variable: "PREFERRED_GEOCODING_PROVIDERS"
- Type: Edgehog.Config.GeocodingProviders
- Default: [Edgehog.Geolocation.Providers.GoogleGeocoding]
- Required: false
- Cached: true

# `preferred_geocoding_providers!`

```elixir
@spec preferred_geocoding_providers!(Skogsra.Env.namespace()) ::
  Edgehog.Config.GeocodingProviders.t() | no_return()
```

A comma separated list of preferred geocoding providers.
Possible values are: google

Bang version of `Edgehog.Config.preferred_geocoding_providers/0` (fails on error). Optionally,
receives the `namespace` for the variable.

# `preferred_geolocation_providers`

```elixir
@spec preferred_geolocation_providers(Skogsra.Env.namespace()) ::
  {:ok, Edgehog.Config.GeolocationProviders.t()} | {:error, binary()}
```

A comma separated list of preferred geolocation providers.
Possible values are: device, google, ipbase.

Calling `Edgehog.Config.preferred_geolocation_providers()` will ensure the following:

- Binding order: [:system, :config]
- OS environment variable: "PREFERRED_GEOLOCATION_PROVIDERS"
- Type: Edgehog.Config.GeolocationProviders
- Default: [Edgehog.Geolocation.Providers.DeviceGeolocation, Edgehog.Geolocation.Providers.GoogleGeolocation, Edgehog.Geolocation.Providers.IPBase]
- Required: false
- Cached: true

# `preferred_geolocation_providers!`

```elixir
@spec preferred_geolocation_providers!(Skogsra.Env.namespace()) ::
  Edgehog.Config.GeolocationProviders.t() | no_return()
```

A comma separated list of preferred geolocation providers.
Possible values are: device, google, ipbase.

Bang version of `Edgehog.Config.preferred_geolocation_providers/0` (fails on error). Optionally,
receives the `namespace` for the variable.

# `preload`

```elixir
@spec preload(Skogsra.Env.namespace()) :: :ok
```

Preloads all variables in a `namespace` if supplied.

# `put_admin_jwk`

```elixir
@spec put_admin_jwk(
  nil | Edgehog.Config.JWTPublicKeyPEMType.t(),
  Skogsra.Env.namespace()
) ::
  :ok | {:error, binary()}
```

Puts the `value` to `Edgehog.Config.admin_jwk/0`. Optionally, receives
the `namespace`.

# `put_authz_provider`

```elixir
@spec put_authz_provider(Edgehog.Config.AuthzProvider.t(), Skogsra.Env.namespace()) ::
  :ok | {:error, binary()}
```

Puts the `value` to `Edgehog.Config.authz_provider/0`. Optionally, receives
the `namespace`.

# `put_database_enable_ssl`

```elixir
@spec put_database_enable_ssl(boolean(), Skogsra.Env.namespace()) ::
  :ok | {:error, binary()}
```

Puts the `value` to `Edgehog.Config.database_enable_ssl/0`. Optionally, receives
the `namespace`.

# `put_database_ssl_cacertfile`

```elixir
@spec put_database_ssl_cacertfile(binary(), Skogsra.Env.namespace()) ::
  :ok | {:error, binary()}
```

Puts the `value` to `Edgehog.Config.database_ssl_cacertfile/0`. Optionally, receives
the `namespace`.

# `put_database_ssl_verify`

```elixir
@spec put_database_ssl_verify(boolean(), Skogsra.Env.namespace()) ::
  :ok | {:error, binary()}
```

Puts the `value` to `Edgehog.Config.database_ssl_verify/0`. Optionally, receives
the `namespace`.

# `put_database_use_os_certs`

```elixir
@spec put_database_use_os_certs(boolean(), Skogsra.Env.namespace()) ::
  :ok | {:error, binary()}
```

Puts the `value` to `Edgehog.Config.database_use_os_certs/0`. Optionally, receives
the `namespace`.

# `put_google_geocoding_api_key`

```elixir
@spec put_google_geocoding_api_key(nil | binary(), Skogsra.Env.namespace()) ::
  :ok | {:error, binary()}
```

Puts the `value` to `Edgehog.Config.google_geocoding_api_key/0`. Optionally, receives
the `namespace`.

# `put_google_geolocation_api_key`

```elixir
@spec put_google_geolocation_api_key(nil | binary(), Skogsra.Env.namespace()) ::
  :ok | {:error, binary()}
```

Puts the `value` to `Edgehog.Config.google_geolocation_api_key/0`. Optionally, receives
the `namespace`.

# `put_ipbase_api_key`

```elixir
@spec put_ipbase_api_key(nil | binary(), Skogsra.Env.namespace()) ::
  :ok | {:error, binary()}
```

Puts the `value` to `Edgehog.Config.ipbase_api_key/0`. Optionally, receives
the `namespace`.

# `put_preferred_geocoding_providers`

```elixir
@spec put_preferred_geocoding_providers(
  Edgehog.Config.GeocodingProviders.t(),
  Skogsra.Env.namespace()
) ::
  :ok | {:error, binary()}
```

Puts the `value` to `Edgehog.Config.preferred_geocoding_providers/0`. Optionally, receives
the `namespace`.

# `put_preferred_geolocation_providers`

```elixir
@spec put_preferred_geolocation_providers(
  Edgehog.Config.GeolocationProviders.t(),
  Skogsra.Env.namespace()
) :: :ok | {:error, binary()}
```

Puts the `value` to `Edgehog.Config.preferred_geolocation_providers/0`. Optionally, receives
the `namespace`.

# `reload_admin_jwk`

```elixir
@spec reload_admin_jwk(Skogsra.Env.namespace()) ::
  {:ok, nil | Edgehog.Config.JWTPublicKeyPEMType.t()} | {:error, binary()}
```

Reloads the value for `Edgehog.Config.admin_jwk/0`. Optionally, receives
the `namespace` for the variable.

# `reload_authz_provider`

```elixir
@spec reload_authz_provider(Skogsra.Env.namespace()) ::
  {:ok, Edgehog.Config.AuthzProvider.t()} | {:error, binary()}
```

Reloads the value for `Edgehog.Config.authz_provider/0`. Optionally, receives
the `namespace` for the variable.

# `reload_database_enable_ssl`

```elixir
@spec reload_database_enable_ssl(Skogsra.Env.namespace()) ::
  {:ok, boolean()} | {:error, binary()}
```

Reloads the value for `Edgehog.Config.database_enable_ssl/0`. Optionally, receives
the `namespace` for the variable.

# `reload_database_ssl_cacertfile`

```elixir
@spec reload_database_ssl_cacertfile(Skogsra.Env.namespace()) ::
  {:ok, binary()} | {:error, binary()}
```

Reloads the value for `Edgehog.Config.database_ssl_cacertfile/0`. Optionally, receives
the `namespace` for the variable.

# `reload_database_ssl_verify`

```elixir
@spec reload_database_ssl_verify(Skogsra.Env.namespace()) ::
  {:ok, boolean()} | {:error, binary()}
```

Reloads the value for `Edgehog.Config.database_ssl_verify/0`. Optionally, receives
the `namespace` for the variable.

# `reload_database_use_os_certs`

```elixir
@spec reload_database_use_os_certs(Skogsra.Env.namespace()) ::
  {:ok, boolean()} | {:error, binary()}
```

Reloads the value for `Edgehog.Config.database_use_os_certs/0`. Optionally, receives
the `namespace` for the variable.

# `reload_google_geocoding_api_key`

```elixir
@spec reload_google_geocoding_api_key(Skogsra.Env.namespace()) ::
  {:ok, nil | binary()} | {:error, binary()}
```

Reloads the value for `Edgehog.Config.google_geocoding_api_key/0`. Optionally, receives
the `namespace` for the variable.

# `reload_google_geolocation_api_key`

```elixir
@spec reload_google_geolocation_api_key(Skogsra.Env.namespace()) ::
  {:ok, nil | binary()} | {:error, binary()}
```

Reloads the value for `Edgehog.Config.google_geolocation_api_key/0`. Optionally, receives
the `namespace` for the variable.

# `reload_ipbase_api_key`

```elixir
@spec reload_ipbase_api_key(Skogsra.Env.namespace()) ::
  {:ok, nil | binary()} | {:error, binary()}
```

Reloads the value for `Edgehog.Config.ipbase_api_key/0`. Optionally, receives
the `namespace` for the variable.

# `reload_preferred_geocoding_providers`

```elixir
@spec reload_preferred_geocoding_providers(Skogsra.Env.namespace()) ::
  {:ok, Edgehog.Config.GeocodingProviders.t()} | {:error, binary()}
```

Reloads the value for `Edgehog.Config.preferred_geocoding_providers/0`. Optionally, receives
the `namespace` for the variable.

# `reload_preferred_geolocation_providers`

```elixir
@spec reload_preferred_geolocation_providers(Skogsra.Env.namespace()) ::
  {:ok, Edgehog.Config.GeolocationProviders.t()} | {:error, binary()}
```

Reloads the value for `Edgehog.Config.preferred_geolocation_providers/0`. Optionally, receives
the `namespace` for the variable.

# `template`

```elixir
@spec template(
  Path.t(),
  keyword()
) :: :ok | {:error, File.posix()}
```

Creates a template for OS environment variables given a `filename`.
Additionally, it can receive a list of options:

- `type`: What kind of file it will generate (`:elixir`, `:unix`,
  `:windows`).
- `namespace`: Namespace for the variables.

# `validate`

```elixir
@spec validate(Skogsra.Env.namespace()) :: :ok | {:error, [binary()]}
```

Validates that all required variables are present.
Returns `:ok` if they are, `{:error, errors}` if they are not. `errors`
will be a list of all errors encountered while getting required variables.

It is possible to provide a `namespace` as argument (defaults to `nil`).

# `validate!`

```elixir
@spec validate!(Skogsra.Env.namespace()) :: :ok | no_return()
```

Validates that all required variables are present.
Returns `:ok` if they are, raises if they're not.

It is possible to provide a `namespace` as argument (defaults to `nil`).

# `validate_admin_authentication!`

```elixir
@spec validate_admin_authentication!() :: :ok | no_return()
```

Validates admin authentication config, raises if invalid.

