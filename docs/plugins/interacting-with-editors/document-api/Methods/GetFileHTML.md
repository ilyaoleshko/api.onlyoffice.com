# GetFileHTML

Returns file content in the HTML format.

## Syntax

```javascript
expression.GetFileHTML();
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Methods.md) class.

## Parameters

This method doesn't have any parameters.

## Returns

string

## Example

```javascript
window.Asc.plugin.executeMethod ("GetFileHTML", null, function (res) {
    console.log (res)
});
```
