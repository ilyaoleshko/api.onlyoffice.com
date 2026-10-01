---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-sdk-js/blob/release/v4.0.0/src/types/index.ts
---

import APITable from '@site/src/components/APITable/APITable';

# TUploadResult

Payload of [TFrameEvents.onUploadSuccess](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFrameEvents.md#onUploadSuccess) in [SDKMode.Forms](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKMode.md#Forms) and [SDKMode.Personal](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKMode.md#Personal):
one object per file transferred with [SDKInstance.upload](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/classes/SDKInstance.md#upload). The same object is the resolved value of `upload`.

```ts
type TUploadResult = object;
```

## Properties

<APITable>

| Property | Type | Description |
| ------ | ------ | ------ |
| `fileName` | `string` | Name of the uploaded file. |
| `fileSize` | `number` | Size of the uploaded file in bytes. |
| `uploadId`? | `number` | Correlation ID the SDK assigned to the `upload` call. |

</APITable>
