---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-sdk-js/blob/release/v4.0.0/src/types/index.ts
---

import APITable from '@site/src/components/APITable/APITable';

# THashSettings

Password hash settings returned by [SDKInstance.getHashSettings](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/classes/SDKInstance.md#gethashsettings).

```ts
type THashSettings = object;
```

## Properties

<APITable>

| Property | Type | Description |
| ------ | ------ | ------ |
| `iterations` | `number` | PBKDF2 iteration count. |
| `salt` | `string` | Base64-encoded salt. |
| `size` | `number` | Hash size in bits. |

</APITable>
