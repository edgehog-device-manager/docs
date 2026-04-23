# `Edgehog.Campaigns.Campaign.Validations.ValidateOperationTypeRequirements`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/campaigns/campaign/validations/validate_operation_type_requirements.ex#L21)

Validates that the required arguments are provided based on the operation type.

For example:
- `firmware_upgrade` operation requires `base_image_id`
- `deployment_deploy`, `deployment_start`, `deployment_stop`, `deployment_delete`
operations require only `release_id`
- `deployment_upgrade` operation requires both `release_id` and `target_release_id`
- `file_download` operation requires `file_id`

