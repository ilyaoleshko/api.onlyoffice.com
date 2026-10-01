---
hide_table_of_contents: true
description: Reset all form fields to empty values.
tags: ["Docs", "Macros", "PDF"]
---

import Video from '@site/src/components/Video/Video';

# Reset all forms

Clears all fields if necessary, for example after printing the document.

```ts
(function()
{
    let doc = Api.GetDocument();
    let allForms = doc.GetAllForms();
    allForms.forEach(form => {
        form.Clear();
    });
})();
```

Methods used: [GetDocument](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/Api/Methods/GetDocument.md), [GetAllForms](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiDocument/Methods/GetAllForms.md), [Clear](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiFormBase/Methods/Clear.md)

## Result

<Video src="https://ilyaoleshko.github.io/assets/video/macros/pdf-editor/reset-all-forms" dark />
