# GetFontList

Returns the fonts list.

## Syntax

```javascript
expression.GetFontList();
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods.md) class.

## Parameters

This method doesn't have any parameters.

## Returns

[FontInfo](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Enumeration/FontInfo.md)[]

## Example

```javascript
window.Asc.plugin.executeMethod ("GetFontList", null, function (res) {
    console.log (res)
});
```
