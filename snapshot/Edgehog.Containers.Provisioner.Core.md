# `Edgehog.Containers.Provisioner.Core`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/provisioner/core.ex#L21)

Convenience module for `Edgehog.Containers.Provisioner.Core.Behaviour`.

The resource specific functions required by the provisioner (both the pure
functions, e.g. `ready?/1` and `topic/1`, and the functions providing the
side effects of the provisioning flow, e.g. `send_to_device/2` and
`reconcile/2`) are not provided by this module: each `Core` module nested
inside a provisioner implements them explicitly, with the details specific to
the resource it provisions.

To use it, it is sufficient to add a using statement like so:

```ex
defmodule ResourceDeploymentProvisioner do
  use Edgehog.Containers.Provisioner, resource: Edgehog.Containers.Resource.Deployment, core: Core

  defmodule Core do
    use Edgehog.Containers.Provisioner.Core
  end
end
```

which will declare that the module implements
`Edgehog.Containers.Provisioner.Core.Behaviour`.

