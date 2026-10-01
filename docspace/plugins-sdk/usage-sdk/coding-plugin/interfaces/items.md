---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-plugin-sdk/blob/release/v4.0.0/tools/constants/sections.mjs
---

# Items

Plugin items that extend specific DocSpace UI locations — context menus, file rows, info panels, profile menus, and navigation buttons.

Choose the item interface that matches the DocSpace UI area you want to extend with your plugin action. Items are registered through the matching [plugin type interface](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/plugins.md). For example, a context menu plugin stores its `IContextMenuItem` objects in a `Map` and returns them from the `getContextMenuItems()` method.

## Overview

Each plugin type has specific items described in this section:

| Interface | Description |
| --- | --- |
| [`IArticleButtonItem`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/items/IArticleButtonItem.md) | Describes a button item that will be embedded in the article sidebar. |
| [`IArticleNavigationItem`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/items/IArticleNavigationItem.md) | Describes a navigation item that will be embedded in the article sidebar as a first-class navigation entry. |
| [`IContextMenuItem`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/items/IContextMenuItem.md) | Describes an item that will be embedded in the context menu. |
| [`IEventListenerItem`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/items/IEventListenerItem.md) | Describes an event listener that reacts to portal events. |
| [`IFileItem`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/items/IFileItem.md) | Describes an item that will be embedded in the file list. |
| [`IInfoPanelItem`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/items/IInfoPanelItem.md) | The info panel item that is displayed in the info panel. |
| [`IMainButtonItem`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/items/IMainButtonItem.md) | Describes an item that will be embedded in the More item of the main button menu. |
| [`IProfileMenuItem`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/items/IProfileMenuItem.md) | Describes an item that will be embedded in the profile menu. |