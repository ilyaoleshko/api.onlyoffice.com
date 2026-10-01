---
sidebar_position: -4
---

# Coding plugin

Develop a plugin. Follow the plugin structure described [here](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/plugin-structure.md).

- Write code for each [plugin type](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/plugins.md) using the corresponding variables, methods and [items](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/items.md). Put the scripts into the *src* folder. Specify the required [Plugin](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/plugins/IPlugin.md) interface for each plugin to be embedded in the portal.

  ![Plugin structure](https://ilyaoleshko.github.io/assets/images/docspace/plugin-structure.png#gh-light-mode-only)![Plugin structure](https://ilyaoleshko.github.io/assets/images/docspace/plugin-structure.dark.png#gh-dark-mode-only)

- Specify [plugin messages](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/utils.md) that will be returned by the items. Use the appropriate [events](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/enums/Actions.md) that will be processed on the portal side.

- Learn which [plugin components](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components.md) can be used for the DocSpace plugin interface and add them to your scripts.

Code samples are available at [GitHub](https://github.com/ONLYOFFICE/docspace-plugins).
