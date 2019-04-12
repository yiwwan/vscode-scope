# Scope

Providing syntax highlighting for scope/usql scripts/views.

## Customizing

A `TM Scope` will be assigned to each part of the file, then corresponding color from the theme will be picked up and used to render the text. You can customize the color used by this extension by overriding it in your config file.

For example, you can patch the themes that haven't provided a color for TM scope `entity.name.type` by putting below snippet in your config file:

```json
"textMateRules": [
    {
        "scope": "entity.name.type.scope",
        "settings": {
            "foreground": "#FF0000"
        }
    }
]
```

### Note

*`parent.child` will derive color from `parent` if color for `parent.child` is not specified.*

*Every TM scope used by this extension will be suffixed with `.scope`, so use `<TM scope>.scope` to make it works on scope files only.*

*You can use `F1` -> `Developer: Inspect TM Scopes` to inspect TM scopes.*

Below are the TM scopes used by this extension.

Token Type | TM Scope
--- | ---
Aggregators | support.function.scope
Comments | comment.line.double-dash.scope, comment.block.scope
Constructor | entity.name.type.scope
Functions | support.function.scope
Keywords | keyword.scope
Parameters | variable.parameter.scope
Preprocessor | meta.preprocessor.scope
Types | keyword.scope, entity.name.type.scope
Strings | string.quoted.double.scope, constant.character.escape.scope