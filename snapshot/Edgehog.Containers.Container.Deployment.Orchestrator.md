# `Edgehog.Containers.Container.Deployment.Orchestrator`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/container/deployment/orchestrator.ex#L21)

Orchestrator for all the provisioner processes of a container.

A container consists of various resources.
- an image
- volumes
- networks
- ...

All these resources have their own provisioner process that supervises the
communication with the device, retrying when some error happens or querying
astarte when triggers might be missing.

This orchestrator is responsible for
- spawning such provisioning processes
- wait for readiness of the various resources
- emit readiness of the whole container when each and every resource finishes
- emit a failure of the whole container when a resource reports a failure

Children are not supervised nor cleaned up by this orchestrator: a child that
crashes is ignored, and a child that gives up (e.g. the maximum number of
retries was hit, the device went offline, or the provisioning timeout was hit)
reports a failure through PubSub, which this orchestrator reacts to.

# `child_spec`

Returns a specification to start this module under a supervisor.

See `Supervisor`.

# `conduct`

Conducts the provisioning of a container deployment.

Starts the orchestrator for the given container deployment under the
`Edgehog.Containers.Container.Deployment.Orchestrator.Supervisor` dynamic
supervisor, which owns the whole provisioning tree of the container (its image,
volumes, networks, device mappings, device requests and their provisioners).

The container orchestrator then:
- spawns the provisioner processes of the container deployment and its
  resources
- waits for the readiness of each and every resource
- emits the readiness of the whole container once all the resources are ready
- marks the container deployment as failed if a resource reports a failure

If the container deployment is already being conducted, the pid of the running
orchestrator is returned and no duplicate orchestrator is started.

Returns `{:ok, pid}` where `pid` is the orchestrator process, or
`{:error, reason}`.

# `name`

# `start_link`

# `topic`

Returns the readiness topic the orchestrator will publish onto when the
resource and its children are ready.

It accepts either an entire %Edgehog.Containers.Container.Deployment{}
resource, or just the ID.

