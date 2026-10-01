---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-sdk-js/blob/release/v4.0.0/src/types/index.ts
---

import APITable from '@site/src/components/APITable/APITable';

# TFrameFilter

Filter and pagination parameters for the file list in [SDKMode.Manager](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKMode.md#Manager) mode.
Passed via [TFrameConfig.filter](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFrameConfig.md#filter) and accepted by [SDKInstance.getRooms](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/classes/SDKInstance.md#getrooms).

```ts
type TFrameFilter = object;
```

## Examples

```typescript
sdk.initFrame({
  mode: "manager",
  filter: { count: "50", sortBy: "AZ", sortOrder: "ascending" },
  ...
});
```

Only the rooms of one room group, e.g. the rooms attached to a CRM deal.
```typescript
sdk.initManager({
  frameId: "ds-frame",
  src: "https://portal.example.com",
  rootPath: "/rooms/shared/",
  filter: { groupId: "42" },
});
```

## Properties

<APITable>

| Property | Type | Description |
| ------ | ------ | ------ |
| `count`? | `string` | Items per page. Default: `"100"`. |
| `folder`? | `string` | Target folder ID. Set automatically when [TFrameConfig.id](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFrameConfig.md#id) is provided in manager mode. |
| `groupId`? | `string` | Room group ID (`GET /api/2.0/files/group`). On the rooms list of [SDKMode.Manager](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKMode.md#Manager) (`rootPath` `/rooms/shared/`) only the rooms of that group are shown, and the group is pinned: search and filters inside the frame stay within it and the group chips are hidden. Also narrows [SDKInstance.getRooms](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/classes/SDKInstance.md#getrooms). Requires ONLYOFFICE Apps 4.0. Unset by default. |
| `page`? | `string` | Page number (1-based). Default: `"1"`. |
| `search`? | `string` | Search query. Empty string = no search. |
| `sortBy`? | [`TFilterSortBy`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFilterSortBy.md) | Sort criterion. See [FilterSortBy](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/FilterSortBy.md). Default: [FilterSortBy.ModifiedDate](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/FilterSortBy.md#ModifiedDate). |
| `sortOrder`? | [`TFilterSortOrder`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFilterSortOrder.md) | Sort direction. See [FilterSortOrder](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/FilterSortOrder.md). Default: [FilterSortOrder.Descending](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/FilterSortOrder.md#Descending). |
| `withSubfolders`? | `boolean` | Include sub-folder contents in search results. Default: `false`. |

</APITable>
