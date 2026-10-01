---
hide_table_of_contents: true
description: Remove all empty tables from a document.
tags: ["Docs", "Macros", "Documents"]
---

import Video from '@site/src/components/Video/Video';

# Remove empty tables

Removes all the empty tables from the document.

```ts
(function () {
    let doc = Api.GetDocument();
    let tables = doc.GetAllTables();

    if (!tables || tables.length === 0) {
        return;
    }

    let removedCount = 0;
    let hasCellText = (cell) => {
        let content = cell.GetContent();
        let paragraphs = content.GetAllParagraphs();

        for (let para of paragraphs) {
            if (para.GetText().trim() !== "") {
                return true;
            }
        }
        return false;
    };

    for (let i = tables.length - 1; i >= 0; i--) {
        let table = tables[i];
        let hasContent = false;

        let rowCount = table.GetRowsCount();
        for (let row = 0; row < rowCount && !hasContent; row++) {
            let cellCount = table.GetRow(row).GetCellsCount();
            for (let cell = 0; cell < cellCount && !hasContent; cell++) {
                if (hasCellText(table.GetCell(row, cell))) {
                    hasContent = true;
                }
            }
        }

        if (!hasContent) {
            table.Delete();
            removedCount++;
        }
    }
})();
```

Methods used: [GetDocument](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/Api/Methods/GetDocument.md), [GetAllTables](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiDocument/Methods/GetAllTables.md), [GetContent](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiTableCell/Methods/GetContent.md), [GetAllParagraphs](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiDocumentContent/Methods/GetAllParagraphs.md), [GetText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiParagraph/Methods/GetText.md), [GetRowsCount](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiTable/Methods/GetRowsCount.md), [GetRow](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiTable/Methods/GetRow.md), [GetCellsCount](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiTableRow/Methods/GetCellsCount.md), [GetCell](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiTable/Methods/GetCell.md), [Delete](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/office-api/usage-api/document-api/ApiTable/Methods/Delete.md)

## Result

<Video src="https://ilyaoleshko.github.io/assets/video/macros/document-editor/remove-empty-tables" dark />
