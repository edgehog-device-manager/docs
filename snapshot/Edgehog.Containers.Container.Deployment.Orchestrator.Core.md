# `Edgehog.Containers.Container.Deployment.Orchestrator.Core`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/container/deployment/orchestrator/core.ex#L21)

Container orchestrator pure functions.

# `container_ready`

Sets container provisioning to :completed

Example:
(%{container_provisioning: :started}) -> %{container_provisioning: :completed}

# `device_mapping_ready`

Removes a device mapping from the list of device mappings that need to be provisioned.

The list of device mappings to be provisioned is expected to be a list of device mapping
deployments in the key `:device_mappings_to_provision` into the state.

Example:
if id matches depl2

(id, %{device_mappings_to_provision: [depl1, depl2, depl3, ...]}) -> %{device_mappings_to_provision: [depl1, depl3, ...]}

# `device_request_ready`

Removes a device request from the list of device requests that need to be provisioned.

The list of device requests to be provisioned is expected to be a list of device request
deployments in the key `:device_requests_to_provision` into the state.

Example:
if id matches depl2

(id, %{device_requests_to_provision: [depl1, depl2, depl3, ...]}) -> %{device_requests_to_provision: [depl1, depl3, ...]}

# `image_ready`

Sets image provisioning to :completed

Example:
(%{image_provisioning: :started}) -> %{image_provisioning: :completed}

# `load_resources`

Loads the necessary resources and puts them in the state.

Returns the state with all the resources loaded in their respective keys.

# `network_ready`

Removes a network from the list of networks that need to be provisioned.

The list of networks to be provisioned is expected to be a list of network
deployments in the key `:networks_to_provision` into the state.

Example:
if id matches depl2

(id, %{networks_to_provision: [depl1, depl2, depl3, ...]}) -> %{networks_to_provision: [depl1, depl3, ...]}

# `provision`

# `ready?`

# `volume_ready`

Removes a volume from the list of volumes that need to be provisioned.

The list of volumes to be provisioned is expected to be a list of volume
deployments in the key `:volumes_to_provision` into the state.

Example:
if id matches depl2

(id, %{volumes_to_provision: [depl1, depl2, depl3, ...]}) -> %{volumes_to_provision: [depl1, depl3, ...]}

