# `Edgehog.Auth.Changes.EraseAlias`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.1/backend/lib/edgehog/auth/changes/erase_alias.ex#L21)

A change to erase the alias for an object in the FGA provider.

Opts:
- alias_attr   :: atom. the attribute to be used as an alias for the resource
- fga_type     :: atom. the type assigned to the resource in the FGA model

An alias is useful, for example, for resources defining an attribute to use for their FGA id that is different than the
their actual id: this way the FGA service can still check programmatically by using the id provided by Ash, but it is
also possible for a human to inspect the status manually.

For example, devices use `device_id` instead of `id`. With this change, the tuples
```fga
  {device:Simpl3D3vice1d, alias, device:<uuid>}
```
and
```fga
  {device:<uuid>, alias, device:Simpl3D3vice1d}
```
will be deleted by the FGA service.

