# `Edgehog.Auth.Changes.WriteRelation`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/auth/changes/write_relation.ex#L21)

A change to write a relation in the FGA provider.

This change expects some opts keys to build the tuple

{ destination_type:destination_id_field(value), relationship, source_type:source_id(value) }

- `destination_type`  :: (optional) is the fga type of the model
- `destination_id`    :: is the realtaionship's destination field to query to get the id of the tuple

- `relationship`      :: is the ash relationship to query to get the destination fields
- `relationship_type` :: (optional) is the actual fga type of the relationship (defaults to the name of the ash relationship)

- `source_type`       :: is the fga type of the source resource
- `source_id`         :: is the field to query to get the correct id to set in the FGA provider.

A lot ! Let's see an example. Suppose we want to set the device <-> realm relationship:

- relationship        : realm (it's called `realm` in the ash resource spec)
- relationship_type   : realm. It's realm _also_ in the fga model! No need to set it twice

- destination_type    : realm, which is the same as the relationship name, no need to set it twice
- destination_id      : the name of the realm (our id is not astarte compatible)

- source_type         : device
- source_id           : device_id (the astarte device id, not our internal id)

Hence:

```elixir
  change {Edgehog.Auth.Changes.WriteRelation destination_id: name, relationship: realm, source_type: :device, source_id: :device_id}
```

With realm "test" and device_id "Simpl3D3vice1d" will write the tuple

```fga
  {realm:test, realm, device:Simpl3D3vice1d}
```

