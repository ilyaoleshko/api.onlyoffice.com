---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-sdk-js/blob/release/v4.0.0/src/types/index.ts
---

import APITable from '@site/src/components/APITable/APITable';

# TSelectedRoom

One selected room in the [SDKMode.RoomSelector](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKMode.md#RoomSelector) payload. [TFrameEvents.onSelectCallback](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFrameEvents.md#onSelectCallback)
receives an **array** of these; other fields of the selector row pass through unchanged.

```ts
type TSelectedRoom = object;
```

## Properties

<APITable>

| Property | Type | Description |
| ------ | ------ | ------ |
| `icon`? | `string` | Room icon URL. |
| `id` | `string` \| `number` | Room ID. |
| `label` | `string` | Room title. |
| `requestTokens`? | [`TRequestTokenInfo`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TRequestTokenInfo.md)[] | External links of a public or shared room; `requestTokens[0].requestToken` is the key for [SDKMode.PublicRoom](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKMode.md#PublicRoom). Absent for rooms without links. |
| `roomType`? | `number` | Numeric room type. See [RoomType](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/RoomType.md). |
| `shared`? | `boolean` | Whether the room has an external link. |

</APITable>
