# GetEditorThemes

Returns the list of available editor themes.

:::note
This functionality is available in paid ONLYOFFICE Docs editions.
:::

## Syntax

```javascript
expression.GetEditorThemes();
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/presentation-api/Methods.md) class.

## Parameters

This method doesn't have any parameters.

## Returns

object[]

## Example

```javascript
window.Asc.plugin.executeMethod("GetEditorThemes", null, function(themes) {
	console.log(themes);
});
```
