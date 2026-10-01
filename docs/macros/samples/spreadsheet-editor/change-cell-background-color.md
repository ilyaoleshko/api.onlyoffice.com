---
hide_table_of_contents: true
description: Change the background color of specified cells.
tags: ["Docs", "Macros", "Spreadsheets"]
---

import Video from '@site/src/components/Video/Video';

# Change cell background color

Sets the background color of the cell **B3** to blue.

```ts
(function()
{
    Api.GetActiveSheet().GetRange("B3").SetFillColor(Api.CreateColorFromRGB(0, 0, 250));
})();
```

Methods used: [GetActiveSheet](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/spreadsheet-api/Api/Methods/GetActiveSheet.md), [GetRange](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/spreadsheet-api/ApiWorksheet/Methods/GetRange.md), [SetFillColor](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/spreadsheet-api/ApiRange/Methods/SetFillColor.md), [CreateColorFromRGB](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/spreadsheet-api/Api/Methods/CreateColorFromRGB.md)

## Reference Microsoft VBA macro code

``` vb
Sub example()
    Range("B3").Interior.Color = RGB(0, 0, 250)
End Sub
```

## Result

<Video src="https://ilyaoleshko.github.io/assets/video/macros/spreadsheet-editor/change-cell-background-color" dark />
