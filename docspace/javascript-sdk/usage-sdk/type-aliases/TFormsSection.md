---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-sdk-js/blob/release/v4.0.0/src/types/index.ts
---

# TFormsSection

Navigation sections available in [SDKMode.Forms](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/enumerations/SDKMode.md#Forms) mode.
Used by [SDKInstance.navigateSection](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/classes/SDKInstance.md#navigatesection).

```ts
type TFormsSection = "my-forms" | "in-progress" | "completed-forms" | "library" | "settings";
```

## Example

```typescript
await instance.navigateSection("completed-forms");
```
