# `Edgehog.Changes.Log`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.1/backend/lib/edgehog/changes/log.ex#L21)

An Ash.Resource.Change that emits a log.

## Options

- `:message`          ::  The message to log. Required for all modes except `:after_transaction`.
- `:log_level`        :: The Logger level to use (e.g., `:info`, `:debug`, `:warning`). Defaults to `:info`.
- `:log_meta`         :: Custom metadata to pass to the Logger. Defaults to `[]`.

## Behavior

The change hooks into the `Ash.Changeset` lifecycle based on the configured `:mode`. 

### Metadata Injection

Regardless of your custom `:log_meta` settings, this change automatically injects the following contextual keys into the Logger metadata if they are available:
* `:tenant` (Extracts the `slug` if an `Edgehog.Tenants.Tenant` struct is present in the context)
* `:resource`
* `:action` (Defaults to `:unknown` if not resolved)
* `:error` (Only injected during failed `:after_transaction` hooks)

## Example

    change {Edgehog.Changes.Log,
      message: "Device created successfully", 
      log_level: :info}

