---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-sdk-js/blob/release/v4.0.0/src/types/index.ts
---

# TCustomActionSection

A section a custom action can be limited to: a [TManagerSection](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TManagerSection.md), a [TPersonalSection](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TPersonalSection.md)
or a [TFormsSection](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFormsSection.md), matched against the mode the frame runs in.

```ts
type TCustomActionSection = 
  | TManagerSection
  | TPersonalSection
  | TFormsSection;
```
