---
hide_table_of_contents: true
description: Insert a text watermark into a document.
tags: ["Docs", "Macros", "Documents"]
---

import Video from '@site/src/components/Video/Video';

# Insert watermark

Inserts or removes a custom watermark on every page of the document.

```ts
(function () {
  let doc = Api.GetDocument();
  let action = "insert"; // Change to "remove" to delete watermark

  if (action === "insert") {
    let watermarkSettings = doc.GetWatermarkSettings();

    watermarkSettings.SetType("text");
    watermarkSettings.SetText("Example Watermark");

    let textProperties = watermarkSettings.GetTextPr();
    textProperties.SetFontFamily("Calibri");
    textProperties.SetFontSize(48);
    textProperties.SetDoubleStrikeout(true);
    textProperties.SetItalic(true);
    textProperties.SetBold(true);
    textProperties.SetUnderline(true);
    textProperties.SetColor(0, 255, 0, false);
    textProperties.SetHighlight("blue");

    watermarkSettings.SetTextPr(textProperties);
    doc.SetWatermarkSettings(watermarkSettings);
  } else if (action === "remove") {
    doc.RemoveWatermark();
  }
})();
```

Methods used: [GetDocument](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/Api/Methods/GetDocument.md), [GetWatermarkSettings](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiDocument/Methods/GetWatermarkSettings.md), [SetType](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiWatermarkSettings/Methods/SetType.md), [SetText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiWatermarkSettings/Methods/SetText.md), [GetTextPr](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiWatermarkSettings/Methods/GetTextPr.md), [SetFontFamily](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiTextPr/Methods/SetFontFamily.md), [SetFontSize](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiTextPr/Methods/SetFontSize.md), [SetDoubleStrikeout](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiTextPr/Methods/SetDoubleStrikeout.md), [SetItalic](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiTextPr/Methods/SetItalic.md), [SetBold](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiTextPr/Methods/SetBold.md), [SetUnderline](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiTextPr/Methods/SetUnderline.md), [SetColor](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiTextPr/Methods/SetColor.md), [SetHighlight](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiTextPr/Methods/SetHighlight.md), [SetTextPr](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiWatermarkSettings/Methods/SetTextPr.md), [SetWatermarkSettings](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiDocument/Methods/SetWatermarkSettings.md), [RemoveWatermark](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiDocument/Methods/RemoveWatermark.md)

## Result

<Video src="https://ilyaoleshko.github.io/assets/video/macros/document-editor/insert-watermark" dark />
