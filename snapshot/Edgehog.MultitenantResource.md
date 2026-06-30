# `Edgehog.MultitenantResource`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.0/backend/lib/edgehog/multitenant_resource.ex#L19)

Define the resource as `belong_to` with a `Edgehog.Tenant.Tenant`.

# Opts
## Types

:tenant_id_in_primary_key?    :: boolean()
:disable_logging              :: boolean()
:fga_type                     :: atom() | nil
:fga_id_attribute             :: atom() | nil

## Description
:tenant_id_in_primary_key?    :: whether the tenant_id is primary key in the relationship
:disable_logging              :: whether to disable debug logging on each action
:fga_type                     :: name of the FGA type for this resource, defined in the model
:fga_id_attribute             :: name of the attribute to be used as FGA id in tuples

`:fga_id_attribute` should be defined only if `:fga_type` is `nil`.
When defined, `:fga_type` should correspond to a type defined in the FGA model,
and `:fga_id_attribute` should be a valid attribute.

