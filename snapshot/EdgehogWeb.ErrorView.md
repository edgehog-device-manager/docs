# `EdgehogWeb.ErrorView`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/edgehog_web/views/error_view.ex#L21)

# `__resource__`

The resource name, as an atom, for this view

# `render`

Renders the given template locally.

# `template_not_found`

```elixir
@spec template_not_found(binary(), map()) :: no_return()
```

Callback invoked when no template is found.
By default it raises but can be customized
to render a particular template.

