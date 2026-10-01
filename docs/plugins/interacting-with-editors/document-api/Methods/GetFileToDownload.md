# GetFileToDownload

Returns the current file to download in the specified format.

## Syntax

```javascript
expression.GetFileToDownload(format);
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Methods.md) class.

## Parameters

| **Name** | **Required/Optional** | **Data type** | **Default** | **Description** |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| format | Optional | string | " " | A format in which you need to download a file. |

## Returns

string

## Example

```javascript
window.Asc.plugin.executeMethod ("GetFileToDownload", ["pdf"], function (res) {
    console.log (res)
});
```
