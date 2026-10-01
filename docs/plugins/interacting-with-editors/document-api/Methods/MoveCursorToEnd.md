# MoveCursorToEnd

Moves a cursor to the end of the current editing area (document body, footer/header, footnote, or autoshape).
This method is similar to pressing the - **Ctrl + End** keyboard shortcut.

## Syntax

```javascript
expression.MoveCursorToEnd(isMoveToMainContent);
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Methods.md) class.

## Parameters

| **Name** | **Required/Optional** | **Data type** | **Default** | **Description** |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| isMoveToMainContent | Required | boolean |  | This flag ignores the current position and always moves a cursor to the end of the document body. |

## Returns

This method doesn't return any data.

## Example

```javascript
window.Asc.plugin.executeMethod ("MoveCursorToEnd", [true]);
```
