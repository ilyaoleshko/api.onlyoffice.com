# AddContentControlCheckBox

Adds an empty content control checkbox to the document.

## Syntax

```javascript
expression.AddContentControlCheckBox(checkBoxPr, commonPr);
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Methods.md) class.

## Parameters

| **Name** | **Required/Optional** | **Data type** | **Default** | **Description** |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| checkBoxPr | Optional | [ContentControlCheckBoxProperties](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Enumeration/ContentControlCheckBoxProperties.md) | \{\} | The content control checkbox properties. |
| commonPr | Optional | [ContentControlProperties](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Enumeration/ContentControlProperties.md) | \{\} | The common content control properties. |

## Returns

This method doesn't return any data.

## Example

```javascript
window.Asc.plugin.executeMethod ("AddContentControlCheckBox", [
    {
        "Checked" : false,
        "CheckedSymbol" : 9756,
        "UncheckedSymbol" : 9744
    },
    {
        "Id" : 7,
        "Tag" : "{tag}",
        "Lock" : 0
    }
]);
```
