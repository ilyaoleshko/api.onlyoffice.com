---
hide_table_of_contents: true
description: Apply conditional formatting rules to a cell range.
tags: ["Docs", "Macros", "Spreadsheets"]
---

import Video from '@site/src/components/Video/Video';

# Conditional formatting rules

Applies multiple conditional formatting rules to the selected range.

```ts
(function () {
    // Get the selected range
    let selectedRanges = Api.GetSelection();

    // Declare colors
    let redColor = Api.CreateColorFromRGB(255, 163, 163);
    let greenColor = Api.CreateColorFromRGB(184, 255, 166);

    selectedRanges.ForEach(function (cellRange) {
        let cellValue = cellRange.GetValue();

        if (!cellValue) {
            return;
        }
        // If value is between 300 and 1000, fill the cell with green
        if (cellValue >= 300 && cellValue <= 1000) {
            cellRange.SetFillColor(greenColor);
        } else if (cellValue < 50) {
            // Else fill the cell with red
            cellRange.SetFillColor(redColor);
        }

        // If value equals zero, add a comment to the cell
        if (cellValue == 0) {
            cellRange.AddComment("Check your formula or inputs, value should not be zero");
        }
    });
})();
```

Methods used: [GetSelection](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/spreadsheet-api/Api/Methods/GetSelection.md), [CreateColorFromRGB](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/spreadsheet-api/Api/Methods/CreateColorFromRGB.md), [ForEach](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/spreadsheet-api/ApiRange/Methods/ForEach.md), [GetValue](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/spreadsheet-api/ApiRange/Methods/GetValue.md), [SetFillColor](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/spreadsheet-api/ApiRange/Methods/SetFillColor.md), [AddComment](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/spreadsheet-api/ApiRange/Methods/AddComment.md)

## Result

<Video src="https://ilyaoleshko.github.io/assets/video/macros/spreadsheet-editor/conditional-formatting-rules" dark />
