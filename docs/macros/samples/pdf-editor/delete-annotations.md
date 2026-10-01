---
hide_table_of_contents: true
description: Remove annotations containing a specified keyword.
tags: ["Docs", "Macros", "PDF"]
---

import Video from '@site/src/components/Video/Video';

# Delete annotations

Iterates through all pages in the PDF document and removes annotations which contain a specified keyword.

```ts
(function () {
  const KEYWORD = "example"; //targeted keyword
  const doc = Api.GetDocument();
  const pagesCount = doc.GetPagesCount();
  let deletedCount = 0;

  for (let i = 0; i < pagesCount; i++) {
    const page = doc.GetPage(i);
    const annots = page.GetAllAnnots();

    for (let j = 0; j < annots.length; j++) {
      const annot = annots[j];
      const contents = ((annot && annot.GetContents()) || "").toLowerCase();

      if (contents.includes(KEYWORD.toLowerCase())) {
        annot.Delete(); //delete annotation
        deletedCount++;
      }
    }
  }

  console.log("Deleted annotations containing keyword:", KEYWORD);
  console.log("Total deleted:", deletedCount);
})();
```

Methods used: [GetDocument](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/pdf-api/Api/Methods/GetDocument.md), [GetPagesCount](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/pdf-api/ApiDocument/Methods/GetPagesCount.md), [GetPage](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/pdf-api/ApiDocument/Methods/GetPage.md), [GetAllAnnots](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/pdf-api/ApiPage/Methods/GetAllAnnots.md), [GetContents](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/pdf-api/ApiBaseAnnotation/Methods/GetContents.md), [Delete](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/pdf-api/ApiBaseAnnotation/Methods/Delete.md)

## Result

<Video src="https://ilyaoleshko.github.io/assets/video/macros/pdf-editor/delete-annotations" dark />
