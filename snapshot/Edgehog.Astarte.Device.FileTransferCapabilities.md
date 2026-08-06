# `Edgehog.Astarte.Device.FileTransferCapabilities`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.1/backend/lib/edgehog/astarte/device/file_transfer_capabilities.ex#L21)

This module defines the `FileTransferCapabilities` struct and implements the
`Edgehog.Astarte.Device.FileTransferCapabilities.Behaviour` to fetch and parse
file transfer capabilities from an Astarte device.

Capabilities are split into global configuration and direction-specific capabilities
(`server_to_device` and `device_to_server`).

The incoming Astarte properties data payload contains:
* A `transfer` map containing global settings like `unixPermissions` and lists of supported
  `targets` for each direction.
* Root-level maps for each direction (e.g., `serverToDevice`, `deviceToServer`) containing
  the specific configurations—such as supported compressed `encodings`—for each target type.

### Parsing Rules

For each known target (`:storage`, `:streaming`, `:filesystem`), the parser applies the
following logic based on the device configuration:

1. Supported with Encodings: If a target string is present within the direction's `targets`
   array, and a corresponding root encoding list exists, it returns the list of encodings
   (e.g., `["tar.gz"]`).
2. Supported without Encodings: If a target string is present within the direction's `targets`
   array but no encoding property is set on the device, it returns an empty list (`[]`).
3. Unsupported: If a target string is entirely absent from the direction's `targets` array,
   it returns `nil`.

# `capabilities`

```elixir
@type capabilities() :: %{optional(target()) =&gt; target_capability()}
```

# `t`

```elixir
@type t() :: %Edgehog.Astarte.Device.FileTransferCapabilities{
  device_to_server: capabilities(),
  server_to_device: capabilities(),
  unix_permissions: boolean() | nil
}
```

# `target`

```elixir
@type target() :: :storage | :streaming | :filesystem
```

# `target_capability`

```elixir
@type target_capability() :: nil | [String.t()]
```

# `parse_data`

