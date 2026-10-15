# `Edgehog.Provisioner.Audit`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/provisioner/audit.ex#L21)

Convenience module for `Edgehog.Provisioner.Audit.Behaviour`.

The resource specific observability functions required by the provisioner
(logging and/or telemetry for each provisioning event) are not provided by
this module: each `Audit` module nested inside a provisioner implements them
explicitly, with the details specific to the resource it provisions.

To use it, it is sufficient to add a using statement like so:

```ex
defmodule ResourceDeploymentProvisioner do
  use Edgehog.Provisioner,
    resource: Edgehog.Containers.Resource.Deployment,
    core: Core,
    audit: Audit
end

defmodule Audit do
  use Edgehog.Provisioner.Audit
end
```

which will declare that the module implements
`Edgehog.Provisioner.Audit.Behaviour`.

