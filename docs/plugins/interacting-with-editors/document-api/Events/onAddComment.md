# onAddComment

The function called when a comment is added to the document with the [AddComment](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Methods/AddComment.md) method.

## Parameters

| **Name** | **Data type** | **Description** |
| --------- | ------------- | ----------- |
| comment | [Event_comment](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/document-api/Enumeration/Event_comment.md) | Defines the comment object containing the comment data. |

## Example

```javascript
window.Asc.plugin.attachEditorEvent("onAddComment", (comment) => {
    console.log("event: onAddComment");
    console.log("Id: " + comment.Id);
    console.log("UserName: " + comment.Data.UserName);
    console.log("Text: " + comment.Data.Text);
    console.log("Time: " + comment.Data.Time);
    console.log("Solved: " + comment.Data.Solved);
    console.log("QuoteText: " + comment.Data.QuoteText);
});
```
