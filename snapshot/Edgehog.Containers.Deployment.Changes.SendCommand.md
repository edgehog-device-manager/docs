# `Edgehog.Containers.Deployment.Changes.SendCommand`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.13.0-rc.0/backend/lib/edgehog/containers/deployment/changes/send_command.ex#L21)

A change to send a command to a deployment _after_ the action has been done.

This ensures that the communication with the device happens only when the
database has been updated with relevant information _and_ in case of success

