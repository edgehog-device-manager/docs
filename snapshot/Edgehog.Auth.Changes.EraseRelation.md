# `Edgehog.Auth.Changes.EraseRelation`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/auth/changes/erase_relation.ex#L21)

A change to delete a relation in the FGA provider.

This change expects some opts keys to build the tuple

{ destination_type:destination_id_field(value), relationship, source_type:source_id(value) }

- `destination_type`  :: (optional) is the fga type of the model
- `destination_id`    :: is the realtaionship's destination field to query to get the id of the tuple

- `relationship`      :: is the ash relationship to query to get the destination fields
- `relationship_type` :: (optional) is the actual fga type of the relationship (defaults to the name of the ash relationship)

- `source_type`       :: is the fga type of the source resource
- `source_id`         :: is the field to query to get the correct id to set in the FGA provider.

For more information and a practical example, see the documentation of `Edgehog.Auth.Changes.WriteRelation`

## Example
```elixir
  change {Edgehog.Auth.Changes.EraseRelation destination_id: :name, relationship: :realm, source_type: :device, source_id: :device_id}
```

Will remove the tuple

```fga
  {realm:test, realm, device:Simpl3D3vice1d}
```

