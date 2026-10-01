---
hide_table_of_contents: true
description: Set a character limit for text form fields.
tags: ["Docs", "Macros", "PDF"]
---

import Video from '@site/src/components/Video/Video';

# Limit number of characters

Restricts the number of characters allowed in text fields whose keys contain a specific keyword.

```ts
(function () {
    // Define a form key and type
    let formKey = "Key";
    let formType = "textForm";
    // Define characters number limit
    let symbolsLimit = 10;
    let doc = Api.GetDocument();
    let forms = doc.GetAllForms();

    for (let form of forms) {
        if (form.GetFormType() === formType && form.GetFormKey() === formKey) {
            let input = form.GetText();
            // Set a tip text to warn a user
            form.SetTipText("Number of symbols should be less than " + symbolsLimit);
            form.SetCharactersLimit(symbolsLimit);
        }
    }
})();
```

Methods used: [GetDocument](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/Api/Methods/GetDocument.md), [GetAllForms](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/form-api/ApiDocument/Methods/GetAllForms.md), [GetFormType](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/form-api/ApiFormBase/Methods/GetFormType.md), [GetFormKey](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/form-api/ApiTextForm/Methods/GetFormKey.md), [GetText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/form-api/ApiTextForm/Methods/GetText.md), [SetTipText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/form-api/ApiTextForm/Methods/SetTipText.md), [SetCharactersLimit](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/form-api/ApiTextForm/Methods/SetCharactersLimit.md)

## Result

<Video src="https://ilyaoleshko.github.io/assets/video/macros/pdf-editor/limit-number-of-characters" dark />
