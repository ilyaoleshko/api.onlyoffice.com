---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-sdk-js/blob/release/v4.0.0/src/errors/index.ts
---

import APITable from '@site/src/components/APITable/APITable';

# SDKError

The SDK's structured error class. Thrown or passed to [TFrameEvents.onAppError](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFrameEvents.md#onAppError)
whenever the SDK encounters a known failure.

The `code` property identifies the failure category; `recoverable` indicates whether
the caller may retry the operation without reinitializing the frame. For
[SDKErrorCode.ApiError](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKErrorCode.md#ApiError) the `status` and `data` properties carry what the portal
reported.

## Example

```typescript
import { SDKError, SDKErrorCode } from '@onlyoffice/docspace-sdk-js';

instance.getFiles().catch((err) => {
  if (err instanceof SDKError) {
    console.error(`[${err.code}] ${err.message}`);
    if (err.recoverable) {
      scheduleRetry();
    }
  }
});
```

## Extends

- `Error`

## Constructors

### Constructor

```ts
new SDKError(
   code: SDKErrorCode, 
   message: string, 
   recoverable?: boolean, 
   details?: TSDKErrorDetails
): SDKError;
```

#### Parameters

<APITable name="Constructor">

| Parameter | Type | Default value | Description |
| ------ | ------ | ------ | ------ |
| `code` | [`SDKErrorCode`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKErrorCode.md) | `undefined` | The error category. Use a [SDKErrorCode](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKErrorCode.md) value. |
| `message` | `string` | `undefined` | Human-readable description of what went wrong. |
| `recoverable` | `boolean` | `false` | Whether the operation may be retried. Default: `false`. |
| `details`? | [`TSDKErrorDetails`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TSDKErrorDetails.md) | `undefined` | HTTP status and portal payload for [SDKErrorCode.ApiError](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKErrorCode.md#ApiError). See [TSDKErrorDetails](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TSDKErrorDetails.md). |

</APITable>

#### Returns

`SDKError`

#### Overrides

```ts
Error.constructor
```

## Properties

<APITable name="SDKError">

| Property | Modifier | Type | Description |
| ------ | ------ | ------ | ------ |
| `code` | `readonly` | [`SDKErrorCode`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKErrorCode.md) | The error category. One of the [SDKErrorCode](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKErrorCode.md) string values. Use this for programmatic branching rather than parsing `message`. |
| `data`? | `readonly` | `object` | The portal's error payload for [SDKErrorCode.ApiError](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKErrorCode.md#ApiError), with `config`, `request` and `stack` removed; `undefined` for every other code. |
| `recoverable` | `readonly` | `boolean` | Whether the caller can retry the failed operation without reinitializing the frame. Default: `false`. |
| `status`? | `readonly` | `number` | HTTP status of the failed portal request. Set for [SDKErrorCode.ApiError](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKErrorCode.md#ApiError) when the portal reported one; `undefined` otherwise. |

</APITable>
