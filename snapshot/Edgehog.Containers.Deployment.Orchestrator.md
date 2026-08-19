# `Edgehog.Containers.Deployment.Orchestrator`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/deployment/orchestrator.ex#L21)

Orchestrator for all provisioner processes of a deployment.

A deployment consists of multiple resources
- a series of containers
- the deployment itself

All these resources have their own process that supervises the communication
with the device, retrying when some error happens or querying astarte when
triggers might be missing.

This orchestrator is responsible for
- spawning such provisioning processes
- wait for readiness of the various resources
- emit readiness of the whole deployment when each and every resource finishes
- mark the deployment as failed when a resource reports a failure

Children are not supervised nor cleaned up by this orchestrator: a child that
crashes is ignored, and a child that gives up (e.g. the maximum number of
retries was hit, the device went offline, or the provisioning timeout was hit)
reports a failure through PubSub, which this orchestrator reacts to. Cleanup
of the provisioning tree on failure is not handled here.

# `child_spec`

Returns a specification to start this module under a supervisor.

See `Supervisor`.

# `conduct`

Conducts the provisioning of a deployment.

Starts the orchestrator for the given deployment under the
`Edgehog.Containers.Deployment.Orchestrator.Supervisor` dynamic supervisor, which
owns the whole provisioning tree of the deployment (its containers and their
provisioners).

The deployment orchestrator then:
- spawns the provisioner processes of the deployment and its resources
- waits for the readiness of each and every resource
- emits the readiness of the whole deployment once all the resources are ready
- marks the deployment as failed if a resource reports a failure

If a deployment is already being conducted, the pid of the running orchestrator
is returned and no duplicate orchestrator is started.

Returns `{:ok, pid}` where `pid` is the orchestrator process, or
`{:error, reason}`.

# `name`

Returns the registered name for the orchestrator of a deployment.

It accepts either an entire `%Edgehog.Containers.Deployment{}` resource, or
just an ID.

# `start_link`

# `topic`

Returns the readiness topic the orchestrator will publish onto when the
deployment and its children are ready.

It accepts either an entire %Edgehog.Containers.Deployment{} resource, or just
an ID.

