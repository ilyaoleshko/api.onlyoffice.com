# Api

Represents the Api class.

## Methods

| Method | Returns | Description |
| ------ | ------- | ----------- |
| [CoAuthoringChatSendMessage](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/CoAuthoringChatSendMessage.md) | None | Sends a message to the co-authoring chat. |
| [EndAction](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/EndAction.md) | None | Specifies the end action for long operations. |
| [FocusEditor](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/FocusEditor.md) | None | Returns focus to the editor. |
| [GetAllComments](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/GetAllComments.md) | comment[] | Returns all the comments from the document. |
| [GetCurrentPage](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/GetCurrentPage.md) | number | Returns the current page index. |
| [GetFileToDownload](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/GetFileToDownload.md) | string | Returns the current file to download in the specified format. |
| [GetFontList](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/GetFontList.md) | [FontInfo](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Enumeration/FontInfo.md)[] | Returns the fonts list. |
| [GetInstalledPlugins](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/GetInstalledPlugins.md) | [PluginData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Enumeration/PluginData.md)[] | Returns all the installed plugins. |
| [GetMacros](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/GetMacros.md) | [Macros](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Enumeration/Macros.md) | Returns the document macros. |
| [GetPageImage](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/GetPageImage.md) | canvas | Returns the page image. |
| [GetSelectedText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/GetSelectedText.md) | string | Returns the selected text from the document. |
| [GetVersion](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/GetVersion.md) | string | Returns the editor version. |
| [GoToPage](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/GoToPage.md) | boolean | Moves to specified page. |
| [InstallPlugin](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/InstallPlugin.md) | object | Installs a plugin using the specified plugin config. |
| [MouseMoveWindow](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/MouseMoveWindow.md) | None | Sends an event to the plugin when the mouse button is moved inside the plugin iframe. |
| [MouseUpWindow](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/MouseUpWindow.md) | None | Sends an event to the plugin when the mouse button is released inside the plugin iframe. |
| [OnDropEvent](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/OnDropEvent.md) | None | Implements the external drag&drop emulation. |
| [PasteHtml](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/PasteHtml.md) | None | Pastes text in the HTML format into the document. |
| [PasteText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/PasteText.md) | None | Pastes text into the document. |
| [RemovePlugin](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/RemovePlugin.md) | object | Removes a plugin with the specified GUID. |
| [ReplacePageContent](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/ReplacePageContent.md) | boolean | Replaces the page content with the specified parameters. |
| [SetMacros](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/SetMacros.md) | None | Sets macros to the document. |
| [SetPluginsOptions](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/SetPluginsOptions.md) | None | Configures plugins from an external source. The settings can be set for all plugins or for a specific plugin. |
| [SetProperties](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/SetProperties.md) | None | Sets the properties to the document. |
| [ShowButton](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/ShowButton.md) | None | Shows or hides buttons in the header. |
| [ShowError](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/ShowError.md) | None | Shows an error/warning message. |
| [ShowInputHelper](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/ShowInputHelper.md) | None | Shows the input helper. |
| [StartAction](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/StartAction.md) | None | Specifies the start action for long operations. |
| [UnShowInputHelper](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/UnShowInputHelper.md) | None | Unshows the input helper. |
| [UpdatePlugin](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/pdf-api/Methods/UpdatePlugin.md) | object | Updates a plugin using the specified plugin config. |
