# `Edgehog.Tenants.Reconciler.Core.DeliveryPolicies`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.1/backend/lib/edgehog/tenants/reconciler/core/delivery_policies.ex#L21)

Edgehog tenant reconciler responsible for delivery policies.

This module has a main entrypoint: `reconcile/1`

`reconcile/1` expects a `Edgehog.Tenants.Reconciler.Core` context with
- a realm management client
- the astarte version

and installs delivery policies accordingly.

It adds a key to the context stating whether delivery polices are compatible or not:

```elixir
delivery_policies_compatible: true | false
```

If errors happen while installing the delivery policies, corresponding entries are added to the context.

```elixir
errors: [delivery_policies: [error1, error2, ...]]
```

# `list_delivery_policies`

Lists all delivery policies under `priv/astarte_resources/delivery_policies`

All returned delivery policies are `EEx` evaluated and `Jason` decoded,
effectively returning a map of all properties of the delivery policy.

# `reconcile`

Given a context, installs the necessary trigger delivery policies.

- first it checks against the recorded astarte version.
- if the minimum required for trigger delivery policies installation is met, then proceeds to install the necessary policies.
- if the minimum required version is not met, then no delivery policies are installed.

A new key is added to the context: `delivery_policies_compatible`, stating
whether astarte is compatible with trigger delivery policies.

Notice: this function might have the side effect of uninstalling all triggers that previously referenced a delivery policy.

Since updating a delivery policy is actually not possible, what we have to do is

- uninstall all the triggers that referenced the old policy
- uninstall the policy
- install the new policy

This leaves the triggers uninstalled, as at this stage we don't have a notion
of what triggers were present in astarte.

# `reconcile_delivery_policy`

