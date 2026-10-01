# GetCurrentSentence

Returns the current sentence.

## Syntax

```javascript
expression.GetCurrentSentence(type);
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Methods.md) class.

## Parameters

| **Name** | **Required/Optional** | **Data type** | **Default** | **Description** |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| type | Optional | [TextPartType](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Enumeration/TextPartType.md) | "entirely" | Specifies if the whole sentence or only its part will be returned. |

## Returns

string

## Example

```javascript
window.Asc.plugin.executeMethod ("GetCurrentSentence", ["entirely"], function (res) {
    console.log (res)
});
```
