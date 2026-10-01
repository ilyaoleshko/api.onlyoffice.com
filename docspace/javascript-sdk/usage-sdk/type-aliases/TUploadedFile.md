---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-sdk-js/blob/release/v4.0.0/src/types/index.ts
---

import APITable from '@site/src/components/APITable/APITable';

# TUploadedFile

A file stored by the [SDKMode.Uploader](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKMode.md#Uploader) dialog: the upload session response of the portal.
Nested in [TUploaderUploadResult.response](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TUploaderUploadResult.md#response).

```ts
type TUploadedFile = object;
```

## Properties

<APITable>

| Property | Type | Description |
| ------ | ------ | ------ |
| `file`? | [`TFileInfo`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFileInfo.md) | The stored file. See [TFileInfo](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFileInfo.md). |
| `folderId`? | `number` | ID of the folder the file was uploaded to. |
| `id`? | `number` | Upload session ID. |
| `providerKey`? | `string` \| `null` | Key of the third-party storage provider, when the folder is a connected storage. |
| `title`? | `string` \| `null` | Title of the stored file, with extension. |
| `uploaded`? | `boolean` | Whether the upload completed. |
| `version`? | `number` | Version number of the stored file. |

</APITable>
