---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-sdk-js/blob/release/v4.0.0/src/errors/index.ts
---

import APITable from '@site/src/components/APITable/APITable';

# SDKErrorCode

Error codes for [SDKError](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/classes/SDKError.md). Each code identifies a specific failure category
in the SDK's iframe communication and lifecycle management.

## Example

```typescript
import { SDKError, SDKErrorCode } from '@onlyoffice/docspace-sdk-js';

try {
  await instance.getFiles();
} catch (err) {
  if (err instanceof SDKError && err.code === SDKErrorCode.Timeout) {
    console.warn('Request timed out — retry?', err.recoverable);
  }
}
```

## Enumeration Members

<APITable>

| Enumeration Member | Value | Description |
| ------ | ------ | ------ |
| `ApiError` | `"API_ERROR"` | The portal reported a failure while executing a method call. [SDKError.status](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/classes/SDKError.md#SDKError-status) carries the HTTP status of the failed request, [SDKError.data](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/classes/SDKError.md#SDKError-data) the portal's error payload. Requires an ONLYOFFICE Apps portal that flags method errors (client 4.0). |
| `CSPViolation` | `"CSP_VIOLATION"` | The host domain is blocked by the ONLYOFFICE Apps Content Security Policy. |
| `Disconnected` | `"DISCONNECTED"` | The iframe is not connected or was disconnected while a call was in flight. |
| `InvalidConfig` | `"INVALID_CONFIG"` | The provided [TFrameConfig](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFrameConfig.md) is missing required fields or has invalid values. |
| `ModeMismatch` | `"MODE_MISMATCH"` | A method was called in an incompatible [SDKMode](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKMode.md) (e.g. [SDKInstance.setCustomActions](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/classes/SDKInstance.md#setcustomactions) outside [SDKMode.Forms](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKMode.md#Forms)), the portal answered that the current mode has no such method, or a session method ([SDKInstance.login](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/classes/SDKInstance.md#login), [SDKInstance.logout](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/classes/SDKInstance.md#logout)) was called in OAuth mode, where the host owns the session. The promise rejects; nothing is thrown synchronously. |
| `ParseError` | `"PARSE_ERROR"` | An incoming postMessage payload could not be parsed as valid JSON. |
| `Timeout` | `"TIMEOUT"` | A method call exceeded its configured timeout ([TFrameConfig.methodTimeout](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFrameConfig.md#methodTimeout)). |
| `TokenResolveFailed` | `"TOKEN_RESOLVE_FAILED"` | The SDK could not resolve an OAuth access token: the [TFrameConfig.getToken](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFrameConfig.md#getToken) callback threw/rejected, or neither `getToken` nor [TFrameConfig.accessToken](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFrameConfig.md#accessToken) was provided in OAuth mode. |
| `UploadFailed` | `"UPLOAD_FAILED"` | A file upload failed or timed out. |

</APITable>
