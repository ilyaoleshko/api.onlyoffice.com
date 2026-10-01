---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-plugin-sdk/blob/release/v4.0.0/tools/constants/sections.mjs
---

# Components

UI components for building plugin interfaces — dialogs, buttons, inputs, and other visual elements. Compose them with `IModalDialog`, `IBox`, or other layout containers; overlays such as dialogs, toasts and selectors are displayed by returning an `IMessage` with the matching [Actions](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/enums/Actions.md) value from an event handler.

## Overview

The following components are available:

| Interface | Description |
| --- | --- |
| [`Component`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/Component.md) | A component that is used to add components into Box. |
| [`IBox`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/IBox.md) | A container that lays out its contents in one direction. |
| [`IButton`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/IButton.md) | A component that is used for an action on a page. |
| [`ICheckbox`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/ICheckbox.md) | Custom checkbox. |
| [`IComboBox`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/IComboBox.md) | Custom combo box input. |
| [`ICreateDialog`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/ICreateDialog.md) | Modal dialog for creating certain item (file, folder, etc.). |
| [`IFloatingOperationsButton`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/IFloatingOperationsButton.md) | Configuration for the floating operations button. |
| [`IFrame`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/IFrame.md) | A component that is used to embed a third-party website into a modal window or the settings page. |
| [`IIconButton`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/IIconButton.md) | A component that displays an interactive icon button with hover and click states. |
| [`IImage`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/IImage.md) | A component that is used to embed an image not from the assets folder into a modal window or the settings page. |
| [`IInput`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/IInput.md) | Input field for single-line strings. |
| [`ILabel`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/ILabel.md) | Field name in the form. |
| [`ILink`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/ILink.md) | Defines the link component properties. |
| [`IMediaViewer`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/IMediaViewer.md) | Properties for the Media Viewer component that allows plugins to display custom content. |
| [`IModalDialog`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/IModalDialog.md) | Modal dialog. |
| [`ISkeleton`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/ISkeleton.md) | A component that is used to hide components during uploading. |
| [`IText`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/IText.md) | Plain text. |
| [`ITextArea`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/ITextArea.md) | Custom textarea. |
| [`IToast`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/IToast.md) | A brief notification that appears on the screen. |
| [`IToggleButton`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/IToggleButton.md) | Custom toggle button input for binary state controls. |
| [`TSelector`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/Selector.md) | Provides selector components for choosing files, rooms, users, and groups within DocSpace. |