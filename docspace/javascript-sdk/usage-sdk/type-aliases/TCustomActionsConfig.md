---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-sdk-js/blob/release/v4.0.0/src/types/index.ts
---

import APITable from '@site/src/components/APITable/APITable';

# TCustomActionsConfig

Custom actions of a frame, set with [TFrameConfig.customActions](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFrameConfig.md#customActions) or [SDKInstance.setCustomActions](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/classes/SDKInstance.md#setcustomactions).

```ts
type TCustomActionsConfig = object;
```

## Example

```typescript
await instance.setCustomActions({
  contextMenu: {
    file: [{ key: "send", label: "Send to CRM" }],
    room: [{ key: "share-contacts", label: "Share to CRM contacts" }],
  },
  createMenu: [{ key: "upload-from-crm", label: "Upload from CRM" }],
});
```

## Properties

<APITable>

| Property | Type | Description |
| ------ | ------ | ------ |
| `contextMenu`? | [`TCustomContextMenuActions`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TCustomContextMenuActions.md) | Context menu actions grouped by entity type. See [TCustomContextMenuActions](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TCustomContextMenuActions.md). |
| `createMenu`? | [`TCustomCreateAction`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TCustomCreateAction.md)[] | Items added to the create ("+") menu. Available in [SDKMode.Manager](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKMode.md#Manager) and [SDKMode.Personal](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKMode.md#Personal). |

</APITable>
