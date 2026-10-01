# IsFillingFormMode

Checks if the document is in the filling form mode.

## Syntax

```javascript
expression.IsFillingFormMode();
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Methods.md) class.

## Parameters

This method doesn't have any parameters.

## Returns

boolean

## Example

```javascript
Asc.plugin.executeMethod('IsFillingFormMode', [], result => console.log('Is filling form mode: ' + result));
```
