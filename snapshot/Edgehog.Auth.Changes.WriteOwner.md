# `Edgehog.Auth.Changes.WriteOwner`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.0/backend/lib/edgehog/auth/changes/write_owner.ex#L21)

A change to assign an owner to a newly created object in the FGA provider.

Opts:
- fga_type     :: atom. the type assigned to the resource in the FGA model

Example tuple:
```fga
  {user:bob, owner, device:Simpl3D3vice1d}
```

