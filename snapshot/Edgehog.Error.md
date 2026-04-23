# `Edgehog.Error`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/error.ex#L19)

Error utilities to match device errors when communicating with astarte.

# `maybe_match_error`

Translates `Astarte.Client.APIError`s into `Edgehog.Error`s, letting `:ok` | `{:ok, value}` be themselves.

## Example

Error.maybe_match_error(:ok, device_id, interface) => :ok
Error.maybe_match_error({:ok, value}, device_id, interface) => {:ok, value}

Error.maybe_match_error({:error, reason}, device_id, interface) => {:error, converted_reason}

