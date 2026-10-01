---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-plugin-sdk/blob/release/v4.0.0/tools/constants/sections.mjs
---

# Plugins

Core plugin interfaces that define the contract for each plugin type supported by DocSpace. Every plugin must implement `IPlugin` plus one or more type-specific interfaces.

Implement the interface that matches the DocSpace UI area you want to extend. Each plugin type registers its UI entries as [items](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/items.md) kept in a `Map`.

## Overview

Available plugin type interfaces:

| Interface | Description |
| --- | --- |
| [`IApiPlugin`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/plugins/IApiPlugin.md) | The plugin that is provided with the origin, proxy, and prefix to make requests to the portal server. |
| [`IArticleButtonPlugin`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/plugins/IArticleButtonPlugin.md) | Describes a plugin that adds custom button items to the article sidebar. |
| [`IArticleNavigationPlugin`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/plugins/IArticleNavigationPlugin.md) | Describes a plugin that adds navigation items to the article sidebar. |
| [`IContextMenuPlugin`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/plugins/IContextMenuPlugin.md) | The plugin that is embedded in the context menu of files, folders, rooms, images, video (audio). |
| [`IEventListenerPlugin`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/plugins/IEventListenerPlugin.md) | The plugin that is given the access to the portal events. |
| [`IFilePlugin`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/plugins/IFilePlugin.md) | The plugin that can interact with the file list. |
| [`IInfoPanelPlugin`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/plugins/IInfoPanelPlugin.md) | The plugin that is embedded as a separate tab in the file info panel. |
| [`IMainButtonPlugin`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/plugins/IMainButtonPlugin.md) | The plugin that can add items to the main button menu. |
| [`IPlugin`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/plugins/IPlugin.md) | The default plugin. |
| [`IPostMessagePlugin`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/plugins/IPostMessagePlugin.md) | The plugin that is given the access to handle postMessage events from iframe components. |
| [`IProfileMenuPlugin`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/plugins/IProfileMenuPlugin.md) | Plugin for embedding items in the profile menu. |
| [`ISettingsPlugin`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/plugins/ISettingsPlugin.md) | The plugin that manages settings for the administrator or owner. |