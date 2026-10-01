---
hide_table_of_contents: true
description: Set a placeholder for combo box fields with a specified key.
tags: ["Docs", "Macros", "PDF"]
---

import Video from '@site/src/components/Video/Video';

# Set placeholder

Sets a specific placeholder for all the combo boxes that have a certain key.

```ts
(function () {
    let key = "MyKey";
    let placeholderText = "Placeholder";
    let doc = Api.GetDocument();

    doc.GetAllForms()
        .filter(field => field.GetFormType() === "comboBoxForm" && field.GetFormKey() === key)
        .forEach(field => field.SetPlaceholderText(placeholderText));
})();
```

Methods used: [GetDocument](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/Api/Methods/GetDocument.md), [GetAllForms](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/form-api/ApiDocument/Methods/GetAllForms.md), [GetFormType](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/form-api/ApiFormBase/Methods/GetFormType.md), [GetFormKey](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/form-api/ApiComboBoxForm/Methods/GetFormKey.md), [SetPlaceholderText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/form-api/ApiComboBoxForm/Methods/SetPlaceholderText.md)

## Result

<Video src="https://ilyaoleshko.github.io/assets/video/macros/pdf-editor/set-placeholder" dark />
