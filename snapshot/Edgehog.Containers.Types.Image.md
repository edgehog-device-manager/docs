# `Edgehog.Containers.Types.Image`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/containers/types/image.ex#L21)

Input type representing an image.

When optional segment fields or `image_credentials_id` are not provided, they
default to `nil` (rather than being omitted). The `Container`
`:create_and_relate` and `:update` actions look images up through the
`:reference_credentials` identity, and Ash only attempts that lookup when
every identity key is present in the input. Absent keys silently create a
duplicate image instead of relating the existing one.

# `handle_change?`

# `prepare_change?`

