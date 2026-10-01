---
description: "TableRow is one row of a table: its cells followed by a last cell with the row's context menu button.\n\nThe Table README describes it in full."
custom_edit_url: "https://github.com/ONLYOFFICE/docspace-ui-kit-react/blob/master/components/table/table-row/TableRow.stories.tsx"
---

import ThemedImage from '@theme/ThemedImage';

# TableRow

TableRow is one row of a table: its cells followed by a last cell with the row's context menu button.

The Table README describes it in full.

<ThemedImage alt="TableRow" width={782} sources={{ light: require('./tablerow--primary-light.png').default, dark: require('./tablerow--primary-dark.png').default }} />

## Props

<ThemedImage alt="TableRow props" width={851} sources={{ light: require('./tablerow--controls-light.png').default, dark: require('./tablerow--controls-dark.png').default }} />

## Stories

### Default

A row with a context menu, the way rows in a file list offer their actions: right-click anywhere in the row, or click the three-dot button at its end.

<ThemedImage alt="Default" width={782} sources={{ light: require('./tablerow--default-light.png').default, dark: require('./tablerow--default-dark.png').default }} />

### Index Editing Mode

While rows are being reordered the last cell with the context menu button is left out, so a drag cannot open a menu by accident (`isIndexEditingMode`).

<ThemedImage alt="Index Editing Mode" width={548} sources={{ light: require('./tablerow--index-editing-mode-light.png').default, dark: require('./tablerow--index-editing-mode-dark.png').default }} />
