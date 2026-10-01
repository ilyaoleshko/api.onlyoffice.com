# GetSelectedOleObjects

Returns an array of the selected OLE objects.

## Syntax

```javascript
expression.GetSelectedOleObjects();
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Methods.md) class.

## Parameters

This method doesn't have any parameters.

## Returns

[OLEProperties](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Enumeration/OLEProperties.md)[]

## Example

```javascript
window.Asc.plugin.executeMethod ("GetSelectedOleObjects");
```
