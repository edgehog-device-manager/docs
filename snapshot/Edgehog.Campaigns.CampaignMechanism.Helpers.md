# `Edgehog.Campaigns.CampaignMechanism.Helpers`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/campaigns/campaign_mechanism/helpers.ex#L21)

Shared helper functions for campaign mechanism implementations.

This module provides common functionality used across different campaign mechanisms,
including deployment operations, timeout handling, and notification processing.

# `application_deployed?`

Checks if an application is deployed on the target device for a given release.

## Parameters
  - target: The deployment target struct.
  - release: The release struct to check.

## Returns
  - `true` if the deployment exists.
  - `false` if the deployment does not exist.
  - Raises an error for unexpected failures.

# `do_retry_target_operation`

Retries a target operation by executing the specified update action on the deployment.

## Parameters
  - target: The deployment target struct.
  - update_action: The action atom to execute (e.g., :start, :stop, :delete, :send_deployment).

## Returns
  - `:ok` if the retry is successful.
  - `{:error, reason}` if the retry fails.

# `link_target_deployment`

Links a target to its deployment based on device and release.

## Parameters
  - target: The deployment target struct.
  - release: The release struct.

## Returns
  - `{:ok, updated_target}` with the deployment linked.

