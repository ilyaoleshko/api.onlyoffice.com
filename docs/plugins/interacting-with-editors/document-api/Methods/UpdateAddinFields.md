# UpdateAddinFields

Updates the addin fields with the specified data.

## Syntax

```javascript
expression.UpdateAddinFields(arrData);
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Methods.md) class.

## Parameters

| **Name** | **Required/Optional** | **Data type** | **Default** | **Description** |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| arrData | Required | [AddinFieldData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Enumeration/AddinFieldData.md)[] |  | An array of addin field data. |

## Returns

This method doesn't return any data.

## Example

```javascript
let addinFieldData = [{"FieldId": "1", "Value": "Addin №1", "Content": "This is the first addin field"}];
window.Asc.plugin.executeMethod("UpdateAddinFields", [addinFieldData]);
```
