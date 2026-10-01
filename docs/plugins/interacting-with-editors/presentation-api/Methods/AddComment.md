# AddComment

Adds a comment to the presentation.

## Syntax

```javascript
expression.AddComment(oCommentData);
```

`expression` - A variable that represents a [Api](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/presentation-api/Methods.md) class.

## Parameters

| **Name** | **Required/Optional** | **Data type** | **Default** | **Description** |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| oCommentData | Required | [CommentData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/presentation-api/Enumeration/CommentData.md) |  | An object which contains the comment data. |

## Returns

string \| null

## Example

```javascript
window.Asc.plugin.executeMethod ("AddComment", [
    {
        "UserName": "John Smith",
        "QuoteText": "text",
        "Text": "comment",
        "Time": "1662737941471",
        "Solved": true,
        "Replies": [
            {
                "UserName": "Mark Potato",
                "Text": "reply 1",
                "Time": "1662740895892",
                "Solved": false
            }
        ]
    }
], function (comment) {
    console.log (comment)
});
```
