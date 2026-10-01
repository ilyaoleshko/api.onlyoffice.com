---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-sdk-js/blob/release/v4.0.0/src/enums/index.ts
---

import APITable from '@site/src/components/APITable/APITable';

# ManagerViewMode

The item layout in [SDKMode.Manager](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKMode.md#Manager) mode.
Passed via [TFrameConfig.viewAs](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFrameConfig.md#viewAs).

## Example

```typescript
sdk.initFrame({ mode: SDKMode.Manager, viewAs: ManagerViewMode.Table, ... });
```

## Enumeration Members

<APITable>

| Enumeration Member | Value | Description |
| ------ | ------ | ------ |
| `Row` | `"row"` | Vertical list — one item per row with details. |
| `Table` | `"table"` | Table with sortable columns. Column visibility is controlled by `viewTableColumns`. |
| `Tile` | `"tile"` | Grid of visual tiles with thumbnails. |

</APITable>
