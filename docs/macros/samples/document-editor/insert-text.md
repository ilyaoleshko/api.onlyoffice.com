---
hide_table_of_contents: true
description: Insert text at the current cursor position.
tags: ["Docs", "Macros", "Documents"]
---

import Video from '@site/src/components/Video/Video';

# Insert text

Inserts text into the document at the current cursor position.

```ts
(function()
{
    let doc = Api.GetDocument();
    let paragraph = Api.CreateParagraph();
    paragraph.AddText("Hello world!");
    doc.InsertContent([paragraph]);
})();
```

Methods used: [GetDocument](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/Api/Methods/GetDocument.md), [CreateParagraph](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/Api/Methods/CreateParagraph.md), [AddText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiParagraph/Methods/AddText.md), [InsertContent](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiDocument/Methods/InsertContent.md)

## Result

<Video src="https://ilyaoleshko.github.io/assets/video/macros/document-editor/insert-text" dark />
