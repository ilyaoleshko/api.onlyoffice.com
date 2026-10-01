---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-sdk-js/blob/release/v4.0.0/src/types/index.ts
---

# TFrameMode

String literal union of all [SDKMode](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKMode.md) values.

Accepted by [TFrameConfig.mode](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFrameConfig.md#mode). Using the [SDKMode](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKMode.md) enum constants
is preferred, but plain string literals (e.g. `"manager"`, `"editor"`) are equally valid.

```ts
type TFrameMode = `${SDKMode}`;
```

## Example

```typescript
sdk.initFrame({ frameId: 'ds-frame', src: 'https://portal.example.com', mode: 'manager' });
// equivalent to:
sdk.initFrame({ frameId: 'ds-frame', src: 'https://portal.example.com', mode: SDKMode.Manager });
```
