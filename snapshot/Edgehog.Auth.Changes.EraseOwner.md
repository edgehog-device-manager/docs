# `Edgehog.Auth.Changes.EraseOwner`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.1/backend/lib/edgehog/auth/changes/erase_owner.ex#L21)

A change to remove the owner of a destroyed object in the FGA provider.

Opts:
- fga_type     :: atom. the type assigned to the resource in the FGA model

Example tuple:
```fga
  {user:bob, owner, device:Simpl3D3vice1d}
```

