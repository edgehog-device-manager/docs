# `Edgehog.Campaigns.Campaign.Changes.ComputeCampaignTargets`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog/campaigns/campaign/changes/compute_campaign_targets.ex#L21)

Computes campaign targets and start campaign executor.

* Firmware upgrade → all updatable devices for the base image
* Deploy operations:
  * deploy → all deployable devices
  * start/stop/upgrade/delete → only devices with the release already deployed

