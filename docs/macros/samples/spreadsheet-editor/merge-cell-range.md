---
hide_table_of_contents: true
description: Merge a range of cells in a spreadsheet.
tags: ["Docs", "Macros", "Spreadsheets"]
---

import Video from '@site/src/components/Video/Video';

# Merge cell range

Merges the selected cell range.

```ts
(function()
{
    Api.GetActiveSheet().GetRange("A1:B3").Merge(true);
})();
```

Methods used: [GetActiveSheet](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/spreadsheet-api/Api/Methods/GetActiveSheet.md), [GetRange](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/spreadsheet-api/ApiWorksheet/Methods/GetRange.md), [Merge](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/spreadsheet-api/ApiRange/Methods/Merge.md)

## Reference Microsoft VBA macro code

``` vb
Sub example()
    Range("A1:B3").Merge
End Sub
```

## Result

<Video src="https://ilyaoleshko.github.io/assets/video/macros/spreadsheet-editor/merge-cell-range" dark />
