# InstallPlugin

Installs a plugin using the specified plugin config.

## Syntax

```javascript
expression.InstallPlugin(config);
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods.md) class.

## Parameters

| **Name** | **Required/Optional** | **Data type** | **Default** | **Description** |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| config | Optional | object |  | The plugin [config](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/configuration.md). |

## Returns

object

## Example

```javascript
window.Asc.plugin.executeMethod ("InstallPlugin", [config], function (result) {
    postMessage (JSON.stringify (result));
});
```
