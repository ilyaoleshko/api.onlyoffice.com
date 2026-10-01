---
hide_table_of_contents: true
description: Format a cell range as a styled table.
tags: ["Docs", "Macros", "Spreadsheets"]
---

import Video from '@site/src/components/Video/Video';

# Format range as table

Formats the range of cells **A1:D10** as a table.

```ts
(function()
{
    Api.GetActiveSheet().FormatAsTable("A1:D10");
})();
```

Methods used: [GetActiveSheet](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/spreadsheet-api/Api/Methods/GetActiveSheet.md), [FormatAsTable](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/spreadsheet-api/ApiWorksheet/Methods/FormatAsTable.md)

## Reference Microsoft VBA macro code

``` vb
Sub example()
    Sheet1.ListObjects.Add(xlSrcRange, Range("A1:D10"), , xlYes).Name = "myTable1"
End Sub
```

## Result

<Video src="https://ilyaoleshko.github.io/assets/video/macros/spreadsheet-editor/format-range-as-a-table" dark />
