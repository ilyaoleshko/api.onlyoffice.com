# GetInstalledPlugins

Returns all the installed plugins.

## Syntax

```javascript
expression.GetInstalledPlugins();
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods.md) class.

## Parameters

This method doesn't have any parameters.

## Returns

[PluginData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Enumeration/PluginData.md)[]

## Example

```javascript
window.Asc.plugin.executeMethod ("GetInstalledPlugins", null, function (result) {
    postMessage (JSON.stringify ({type: 'InstalledPlugins', data: result }));
});
```
