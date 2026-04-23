# `Edgehog.Error.DeviceOffline`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/error/device_offline.ex#L21)

Used when requests to a device fail because the device appears offline.

# `exception`

```elixir
@spec exception(opts :: Keyword.t()) :: %Edgehog.Error.DeviceOffline{
  __exception__: true,
  bread_crumbs: term(),
  class: term(),
  device_id: term(),
  interface: term(),
  path: term(),
  splode: term(),
  stacktrace: term(),
  vars: term()
}
```

Create an `Elixir.Edgehog.Error.DeviceOffline` without raising it.

## Keys

- :interface
- :device_id

