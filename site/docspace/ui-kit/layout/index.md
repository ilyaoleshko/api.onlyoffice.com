---
custom_edit_url: "https://github.com/ONLYOFFICE/docspace-ui-kit-react/blob/master/scripts/docs/sections.mjs"
---

# Layout

The page's plumbing: portals, scroll areas, the selection rectangle and the theme wrapper.

## Overview

The following components are available:

| Component | Description |
| --- | --- |
| [`Portal`](./portal.md) | Renders a node into another part of the document, after mount, keeping it inside the React tree. |
| [`Scrollbar`](./scrollbar.md) | Scrolling region with the kit's own thin tracks, which fade out when nothing is happening. |
| [`SelectionArea`](./selection-area.md) | Rubber-band selection: a dragged rectangle that reports which items it covers, frame by frame. |
| [`ThemeProviderComponent`](./theme-provider.md) | The older theme provider: it writes the theme onto the document and supplies the kit's theme context. |
