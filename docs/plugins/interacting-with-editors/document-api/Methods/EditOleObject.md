# EditOleObject

Edits an OLE object in the document.

## Syntax

```javascript
expression.EditOleObject(data);
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Methods.md) class.

## Parameters

| **Name** | **Required/Optional** | **Data type** | **Default** | **Description** |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| data | Required | [OLEProperties](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Enumeration/OLEProperties.md) |  | The OLE object properties. |

## Returns

This method doesn't return any data.

## Example

```javascript
var _param = {
    "data": "{data}",
    "imgSrc": "https://example.com/image.png",
    "objectId": "5_556",
    "width": 70,
    "height": 70,
    "widthPix": 60 * 36000,
    "heightPix": 60 * 36000
};
window.Asc.plugin.executeMethod ("EditOleObject", [_param], function () {
    window.Asc.plugin.executeCommand ("close", "");
});
```
