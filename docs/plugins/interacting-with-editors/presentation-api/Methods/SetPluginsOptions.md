# SetPluginsOptions

Configures plugins from an external source. The settings can be set for all plugins or for a specific plugin.
For example, this method can be used to pass an authorization token to the plugin. This method can be used only with the connector class.

## Syntax

```javascript
expression.SetPluginsOptions(options);
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/presentation-api/Methods.md) class.

## Parameters

| **Name** | **Required/Optional** | **Data type** | **Default** | **Description** |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| options | Required | [PluginOptions](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/presentation-api/Enumeration/PluginOptions.md) |  | Plugin options. |

## Returns

This method doesn't return any data.
