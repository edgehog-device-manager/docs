# `Edgehog.Error.AstarteAPIError`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/error/astarte_api_error.ex#L21)

Used when Astarte replies with an APIError

# `exception`

```elixir
@spec exception(opts :: Keyword.t()) :: %Edgehog.Error.AstarteAPIError{
  __exception__: true,
  bread_crumbs: term(),
  class: term(),
  device_id: term(),
  interface: term(),
  path: term(),
  response: term(),
  splode: term(),
  stacktrace: term(),
  status: term(),
  vars: term()
}
```

Create an `Elixir.Edgehog.Error.AstarteAPIError` without raising it.

## Keys

- :status
- :response
- :device_id
- :interface

