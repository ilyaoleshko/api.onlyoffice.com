# SetEditingRestrictions

Sets the document editing restrictions.

## Syntax

```javascript
expression.SetEditingRestrictions(restrictions);
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Methods.md) class.

## Parameters

| **Name** | **Required/Optional** | **Data type** | **Default** | **Description** |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| restrictions | Required | [DocumentEditingRestrictions](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Enumeration/DocumentEditingRestrictions.md) |  | The document editing restrictions. |

## Returns

This method doesn't return any data.

## Example

```javascript
window.Asc.plugin.executeMethod("SetEditingRestrictions", ["readOnly"]);
```
