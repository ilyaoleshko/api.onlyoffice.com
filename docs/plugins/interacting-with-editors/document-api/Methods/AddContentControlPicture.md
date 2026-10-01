# AddContentControlPicture

Adds an empty content control picture to the document.

## Syntax

```javascript
expression.AddContentControlPicture(commonPr);
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Methods.md) class.

## Parameters

| **Name** | **Required/Optional** | **Data type** | **Default** | **Description** |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| commonPr | Optional | [ContentControlProperties](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Enumeration/ContentControlProperties.md) | \{\} | The common content control properties. |

## Returns

This method doesn't return any data.

## Example

```javascript
window.Asc.plugin.executeMethod ("AddContentControlPicture", [{"Id" : 7, "Tag" : "{tag}", "Lock" : 0}]);
```
