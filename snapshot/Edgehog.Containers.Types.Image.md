# `Edgehog.Containers.Types.Image`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.0/backend/lib/edgehog/containers/types/image.ex#L21)

Input type representing an image.

When `image_credentials_id` is not provided, it defaults to `nil`
(rather than being omitted). The `Container` `:create_and_relate` action
looks images up through the `:reference_credentials` identity, and Ash
only attempts that lookup when every identity key is present in the
input. Absent keys silently create a duplicate image instead of
relating the existing one.

# `handle_change?`

# `prepare_change?`

