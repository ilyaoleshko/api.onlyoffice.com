# GetCurrentAddinField

Returns the current addin field from the document.

## Syntax

```javascript
expression.GetCurrentAddinField();
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Methods.md) class.

## Parameters

This method doesn't have any parameters.

## Returns

[AddinFieldData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Enumeration/AddinFieldData.md)

## Example

```javascript
window.Asc.plugin.executeMethod("GetCurrentAddinField", [], function(data){
	if (null === data) {
		console.log("No addin field at the current cursor position");
	} else {
		console.log("Current addin field:", data);
	}
});
```
