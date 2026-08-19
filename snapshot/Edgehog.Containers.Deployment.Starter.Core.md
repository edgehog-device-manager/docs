# `Edgehog.Containers.Deployment.Starter.Core`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.1/backend/lib/edgehog/containers/deployment/starter/core.ex#L21)

Deployment starter core functions.

This is a collection of pure functions that handle the business logic. They
primarily are functions that interact with other parts of the application
(e.g., read the database, send signals, subscribe to events, etc.).

# `load`

Loads pending deployments into the state.

given a device and a tenant scope returns the list of deployments `:pending`
for that device and tenant.

Example:
```elixir
> device = %Device{device_id: "some-device-id"}
> tenant = %Tenant{}

> Core.load(device, tenant)
[
  %Deployment{},
  %Deployment{},
  ...
]
```

# `log_errors`

Logs all the errors given as first argument. The errors must follow the
`{:error, error, deployment}` convention, so that it's understandable for which
deployment the error was generated.

# `start`

Starts all given deployment. For each deployment the orchestrator will be called.

returns the list of errors generated while starting each deployment in the shape
`{:error, error, deployment}`.

