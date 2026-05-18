# `Edgehog.Changes.Log`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/changes/log.ex#L21)

An Ash.Resource.Change that emits a log entry at a specified hook lifecycle.

## Options

- `:mode`             :: (Required) Determines *when* to emit the log. 
  Supported modes match the underlying `Ash.Changeset` lifecycle hooks:
  + `:before_action`
  + `:before_transaction`
  + `:after_action`
  + `:after_transaction`
- `:message`          ::  The message to log. Required for all modes except `:after_transaction`.
- `:message_success`  :: The message to log if a transaction succeeds. Required for `:after_transaction` mode.
- `:message_fail`     :: The message to log if a transaction fails. Required for `:after_transaction` mode.
- `:log_level`        :: The Logger level to use (e.g., `:info`, `:debug`, `:warning`). Defaults to `:info`.
- `:log_meta`         :: Custom metadata to pass to the Logger. Defaults to `[]`.

## Behavior

The change hooks into the `Ash.Changeset` lifecycle based on the configured `:mode`. 

### Metadata Injection

Regardless of your custom `:log_meta` settings, this change automatically injects the following contextual keys into the Logger metadata if they are available:
* `:tenant` (Extracts the `slug` if an `Edgehog.Tenants.Tenant` struct is present in the context)
* `:domain`
* `:resource`
* `:action` (Defaults to `:unknown` if not resolved)
* `:error` (Only injected during failed `:after_transaction` hooks)

### Message Resolution
* `:before_action`, `:before_transaction`, and `:after_action` hooks exclusively evaluate the `:message` option.
* `:after_transaction` evaluates either `:message_success` or `:message_fail` depending on the outcome of the transaction.

## Example

    change {Edgehog.Changes.Log, mode: :before_action, message: "Creating a new device..."}
    
    change {Edgehog.Changes.Log, 
      mode: :after_transaction, 
      message_success: "Device created successfully", 
      message_fail: "Failed to create device",
      log_level: :error}

