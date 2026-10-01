# CDocBuilderContextScope

The stack-allocated class used by ONLYOFFICE Document Builder which sets the execution context for all operations executed within a local scope. All opened scopes will be closed automatically when the builder [CloseFile](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilder/CloseFile.md) method is called.

## Syntax

```cpp
class CDocBuilderContextScope
```

## Methods

| Name              | Description               |
| ----------------- | ------------------------- |
| [Close](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderContextScope/Close.md) | Closes the current scope. |

:::note
**Java** uses camelCase method names: `close`.
:::
