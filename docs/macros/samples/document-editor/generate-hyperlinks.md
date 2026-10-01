---
hide_table_of_contents: true
description: Generate hyperlinks from URLs found in text.
tags: ["Docs", "Macros", "Documents"]
---

import Video from '@site/src/components/Video/Video';

# Generate hyperlinks

Generates and inserts hyperlinks instead of text URLs.

```ts
(function()
{
    //Use regular expression to find and replace URLs
    let urlRegex = /(https?:\/\/[^\s]+)/g;
    let doc = Api.GetDocument();
    //Get all paragraphs to update
    let allParagraphs = doc.GetAllParagraphs();

    allParagraphs.forEach(paragraph => {
        let rawText = paragraph.GetText();
        //Clear all content after getting text
        paragraph.RemoveAllElements();

        //Split text by url parts
        let parts = rawText.split(urlRegex);

        parts.forEach(part => {
            if (urlRegex.test(part)) {
                //Add hyperlink if regular expression matches the part
                let hyperlinkRun = Api.CreateRun();
                hyperlinkRun.AddText(part);
                paragraph.AddElement(hyperlinkRun);
                hyperlinkRun.AddHyperlink(part);
            } else {
                //Add text if regular expression does not match
                let textRun = Api.CreateRun();
                textRun.AddText(part);
                paragraph.AddElement(textRun);
            }
        });
    });
})();
```

Methods used: [GetDocument](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/Api/Methods/GetDocument.md), [GetAllParagraphs](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiDocument/Methods/GetAllParagraphs.md), [GetText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiParagraph/Methods/GetText.md), [RemoveAllElements](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiParagraph/Methods/RemoveAllElements.md), [CreateRun](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/Api/Methods/CreateRun.md), [AddText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiRun/Methods/AddText.md), [AddElement](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiParagraph/Methods/AddElement.md), [AddHyperlink](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiRun/Methods/AddHyperlink.md)

## Result

<Video src="https://ilyaoleshko.github.io/assets/video/macros/document-editor/generate-hyperlinks" dark />
