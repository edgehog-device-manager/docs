# `Edgehog.Tenants.Reconciler.Core`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.1/backend/lib/edgehog/tenants/reconciler/core.ex#L21)

Tenants reconciler module.

This module provides the core functionality of the reconciler, such as list
all delivery policies, build and install triggers, install interfaces etc.

The main function is `reconcile/1`.

`reconcile/1` takes a valid tenant and reconciles it as follows:

1. checks the astarte version. This impacts what can and cannot be installed:
   + version >= 1.1.1      => astarte supports trigger delivery policies.
   + version >= 1.3.0-rc.0 => astarte supports device registration and device deletion triggers
2. installs trigger delivery policies (if the astarte version supports it)
3. installs astarte interfaces
4. installs triggers (if supported and with delivery policies if supported)

# `reconcile`

