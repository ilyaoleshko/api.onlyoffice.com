# SelectAddinField

Selects the specified add-in field.

## Syntax

```javascript
expression.SelectAddinField(fieldId);
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Methods.md) class.

## Parameters

| **Name** | **Required/Optional** | **Data type** | **Default** | **Description** |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| fieldId | Required | string |  | Field identifier. |

## Returns

This method doesn't return any data.

## Example

```javascript
let fieldId = "12";
window.Asc.plugin.executeMethod("SelectAddinField", [fieldId]);
```
