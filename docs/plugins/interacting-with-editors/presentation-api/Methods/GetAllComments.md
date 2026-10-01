# GetAllComments

Returns all the comments from the document.

## Syntax

```javascript
expression.GetAllComments();
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/presentation-api/Methods.md) class.

## Parameters

This method doesn't have any parameters.

## Returns

[comment](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/presentation-api/Enumeration/comment.md)[]

## Example

```javascript
window.Asc.plugin.executeMethod ("GetAllComments", null, function (comments) {
    Comments = comments;
    addComments (comments);
});
```
