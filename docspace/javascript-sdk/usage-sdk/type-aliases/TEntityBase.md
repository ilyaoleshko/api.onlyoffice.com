---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-sdk-js/blob/release/v4.0.0/src/types/index.ts
---

import APITable from '@site/src/components/APITable/APITable';

# TEntityBase

Common fields shared by file, folder, and room metadata.
Extended by [TFileInfo](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFileInfo.md), [TFolderInfo](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFolderInfo.md), and [TRoomInfo](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TRoomInfo.md).

```ts
type TEntityBase = object;
```

## Properties

<APITable>

| Property | Type | Description |
| ------ | ------ | ------ |
| `access` | `number` | Numeric access level. |
| `canShare` | `boolean` | Whether the entity can be shared. |
| `created` | `string` | ISO 8601 creation date. |
| `createdBy` | [`TCreatedBy`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TCreatedBy.md) | Creator reference. |
| `id` | `number` | Entity ID. |
| `mute` | `boolean` | Whether notifications are muted. |
| `security` | `Record`\<`string`, `boolean`\> | Permission flags. |
| `shared` | `boolean` | Whether the entity is shared. |
| `title` | `string` | Display name. |
| `updated` | `string` | ISO 8601 last update date. |
| `updatedBy` | [`TCreatedBy`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TCreatedBy.md) | Last editor reference. |

</APITable>
