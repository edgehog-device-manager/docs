# `Edgehog.Astarte.Device.ResourceEvent.Data`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/astarte/device/resource_event/data.ex#L21)

Data astarte sends on a resource event.

# `t`

```elixir
@type t() :: %Edgehog.Astarte.Device.ResourceEvent.Data{
  add_info: [String.t()],
  message: String.t(),
  status: String.t() | nil,
  timestamp: DateTime.t() | nil
}
```

