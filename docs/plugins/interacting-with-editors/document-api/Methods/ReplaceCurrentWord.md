# ReplaceCurrentWord

Replaces the current word with the specified string.

## Syntax

```javascript
expression.ReplaceCurrentWord(replaceString, type);
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Methods.md) class.

## Parameters

| **Name** | **Required/Optional** | **Data type** | **Default** | **Description** |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| replaceString | Required | string |  | Replacement string. |
| type | Optional | [TextPartType](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Enumeration/TextPartType.md) | "entirely" | Specifies if the whole word or only its part will be replaced. |

## Returns

This method doesn't return any data.

## Example

```javascript
window.Asc.plugin.executeMethod ("ReplaceCurrentWord", ["ONLYOFFICE", "entirely"]);
```
