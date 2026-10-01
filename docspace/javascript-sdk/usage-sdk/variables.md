---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-sdk-js/blob/release/v4.0.0/tools/docs/sections.mjs
---

# Variables

Exported constants: the default frame configuration, the iframe name prefix, the CSP validation endpoint and the error messages the SDK shows.

## Overview

The following constants are available:

| Constant | Description |
| --- | --- |
| [`connectErrorText`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/variables/connectErrorText.md) | Error message passed to [TFrameEvents.onAppError](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/type-aliases/TFrameEvents.md#onAppError) when a method is called before the postMessage channel is established (i.e. before the first valid message from the iframe). |
| [`CSPApiUrl`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/variables/CSPApiUrl.md) | The ONLYOFFICE Apps CSP validation endpoint. |
| [`cspErrorText`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/variables/cspErrorText.md) | Error message shown when the host domain is not in the ONLYOFFICE Apps CSP allowlist. |
| [`defaultConfig`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/variables/defaultConfig.md) | The default configuration applied to every frame before user overrides. |
| [`FRAME_NAME`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/javascript-sdk/usage-sdk/variables/FRAME_NAME.md) | The prefix for iframe `name` attribute. |
