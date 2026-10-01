# Api

Represents the Api class.

## Methods

| Method | Returns | Description |
| ------ | ------- | ----------- |
| [AddComment](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/AddComment.md) | string \| null | Adds a comment to the workbook. |
| [AddOleObject](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/AddOleObject.md) | None | Adds an OLE object to the current document position. |
| [ChangeComment](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/ChangeComment.md) | boolean | Changes the specified comment. |
| [CoAuthoringChatSendMessage](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/CoAuthoringChatSendMessage.md) | None | Sends a message to the co-authoring chat. |
| [EditOleObject](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/EditOleObject.md) | None | Edits an OLE object in the document. |
| [EndAction](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/EndAction.md) | None | Specifies the end action for long operations. |
| [FocusEditor](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/FocusEditor.md) | None | Returns focus to the editor. |
| [GetAllComments](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/GetAllComments.md) | [comment](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Enumeration/comment.md)[] | Returns all the comments from the document. |
| [GetCustomFunctions](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/GetCustomFunctions.md) | string | Returns a library of local custom functions. |
| [GetFileToDownload](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/GetFileToDownload.md) | string | Returns the current file to download in the specified format. |
| [GetFontList](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/GetFontList.md) | [FontInfo](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Enumeration/FontInfo.md)[] | Returns the fonts list. |
| [GetImageDataFromSelection](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/GetImageDataFromSelection.md) | [ImageData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Enumeration/ImageData.md) | Returns the image data from the first of the selected drawings. If there are no drawings selected, the method returns a white rectangle. |
| [GetInstalledPlugins](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/GetInstalledPlugins.md) | [PluginData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Enumeration/PluginData.md)[] | Returns all the installed plugins. |
| [GetMacros](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/GetMacros.md) | [Macros](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Enumeration/Macros.md) | Returns the document macros. |
| [GetSelectedContent](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/GetSelectedContent.md) | string | Returns the selected content in the specified format. |
| [GetSelectedOleObjects](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/GetSelectedOleObjects.md) | [OLEProperties](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Enumeration/OLEProperties.md)[] | Returns an array of the selected OLE objects. |
| [GetSelectedText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/GetSelectedText.md) | string | Returns the selected text from the document. |
| [GetSelectionType](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/GetSelectionType.md) | [SelectionType](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Enumeration/SelectionType.md) | Returns the type of the current selection. |
| [GetVBAMacros](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/GetVBAMacros.md) | string \| null | Returns all VBA macros from the document. |
| [GetVersion](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/GetVersion.md) | string | Returns the editor version. |
| [InputText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/InputText.md) | None | Inserts text into the document. |
| [InstallPlugin](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/InstallPlugin.md) | object | Installs a plugin using the specified plugin config. |
| [MouseMoveWindow](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/MouseMoveWindow.md) | None | Sends an event to the plugin when the mouse button is moved inside the plugin iframe. |
| [MouseUpWindow](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/MouseUpWindow.md) | None | Sends an event to the plugin when the mouse button is released inside the plugin iframe. |
| [OnDropEvent](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/OnDropEvent.md) | None | Implements the external drag&drop emulation. |
| [OnEncryption](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/OnEncryption.md) | None | Encrypts the document. |
| [PasteHtml](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/PasteHtml.md) | None | Pastes text in the HTML format into the document. |
| [PasteText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/PasteText.md) | None | Pastes text into the document. |
| [PutImageDataToSelection](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/PutImageDataToSelection.md) | None | Replaces the first selected drawing with the image specified in the parameters. |
| [RemoveComments](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/RemoveComments.md) | None | Removes the specified comments. |
| [RemoveOleObject](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/RemoveOleObject.md) | None | Removes the OLE object from the workbook by its internal ID. |
| [RemovePlugin](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/RemovePlugin.md) | object | Removes a plugin with the specified GUID. |
| [ReplaceTextSmart](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/ReplaceTextSmart.md) | boolean | Replaces each paragraph (or text in cell) in the select with the corresponding text from an array of strings. |
| [SetCustomFunctions](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/SetCustomFunctions.md) | None | Updates a library of local custom functions. |
| [SetMacros](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/SetMacros.md) | None | Sets macros to the document. |
| [SetPluginsOptions](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/SetPluginsOptions.md) | None | Configures plugins from an external source. The settings can be set for all plugins or for a specific plugin. |
| [SetProperties](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/SetProperties.md) | None | Sets the properties to the document. |
| [ShowButton](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/ShowButton.md) | None | Shows or hides buttons in the header. |
| [ShowError](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/ShowError.md) | None | Shows an error/warning message. |
| [ShowInputHelper](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/ShowInputHelper.md) | None | Shows the input helper. |
| [StartAction](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/StartAction.md) | None | Specifies the start action for long operations. |
| [UnShowInputHelper](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/UnShowInputHelper.md) | None | Unshows the input helper. |
| [UpdatePlugin](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/spreadsheet-api/Methods/UpdatePlugin.md) | object | Updates a plugin using the specified plugin config. |
