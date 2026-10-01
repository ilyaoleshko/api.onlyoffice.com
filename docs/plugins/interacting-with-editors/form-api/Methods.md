# Api

Represents the Api class.

## Methods

| Method | Returns | Description |
| ------ | ------- | ----------- |
| [AddOleObject](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/AddOleObject.md) | None | Adds an OLE object to the current document position. |
| [CoAuthoringChatSendMessage](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/CoAuthoringChatSendMessage.md) | None | Sends a message to the co-authoring chat. |
| [ConvertDocument](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/ConvertDocument.md) | string | Converts a document to Markdown or HTML text. |
| [EditOleObject](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/EditOleObject.md) | None | Edits an OLE object in the document. |
| [EndAction](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/EndAction.md) | None | Specifies the end action for long operations. |
| [FocusEditor](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/FocusEditor.md) | None | Returns focus to the editor. |
| [GetAllForms](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/GetAllForms.md) | [ContentControl](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Enumeration/ContentControl.md)[] | Returns information about all the forms that have been added to the document. |
| [GetDocumentLang](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/GetDocumentLang.md) | string | Returns the document language. |
| [GetFileToDownload](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/GetFileToDownload.md) | string | Returns the current file to download in the specified format. |
| [GetFontList](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/GetFontList.md) | [FontInfo](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Enumeration/FontInfo.md)[] | Returns the fonts list. |
| [GetFormValue](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/GetFormValue.md) | null \| string \| boolean | Returns a value of the specified form. |
| [GetFormsByTag](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/GetFormsByTag.md) | [ContentControl](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Enumeration/ContentControl.md)[] | Returns information about all the forms that have been added to the document with specified tag. |
| [GetImageDataFromSelection](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/GetImageDataFromSelection.md) | [ImageData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Enumeration/ImageData.md) | Returns the image data from the first of the selected drawings. If there are no drawings selected, the method returns a white rectangle. |
| [GetInstalledPlugins](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/GetInstalledPlugins.md) | [PluginData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Enumeration/PluginData.md)[] | Returns all the installed plugins. |
| [GetMacros](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/GetMacros.md) | [Macros](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Enumeration/Macros.md) | Returns the document macros. |
| [GetSelectedContent](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/GetSelectedContent.md) | string | Returns the selected content in the specified format. |
| [GetSelectedOleObjects](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/GetSelectedOleObjects.md) | [OLEProperties](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Enumeration/OLEProperties.md)[] | Returns an array of the selected OLE objects. |
| [GetSelectedText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/GetSelectedText.md) | string | Returns the selected text from the document. |
| [GetSelectionType](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/GetSelectionType.md) | [SelectionType](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Enumeration/SelectionType.md) | Returns the type of the current selection. |
| [GetVBAMacros](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/GetVBAMacros.md) | string \| null | Returns all VBA macros from the document. |
| [GetVersion](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/GetVersion.md) | string | Returns the editor version. |
| [InputText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/InputText.md) | None | Inserts text into the document. |
| [InstallPlugin](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/InstallPlugin.md) | object | Installs a plugin using the specified plugin config. |
| [IsEditingOFormMode](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/IsEditingOFormMode.md) | boolean | Checks if the document is in the editing OForm mode. |
| [IsFillingFormMode](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/IsFillingFormMode.md) | boolean | Checks if the document is in the filling form mode. |
| [IsFillingOFormMode](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/IsFillingOFormMode.md) | boolean | Checks if the document is in the filling OForm mode. |
| [IsFormSigned](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/IsFormSigned.md) | boolean | Checks whether the specified form has been digitally signed. |
| [MouseMoveWindow](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/MouseMoveWindow.md) | None | Sends an event to the plugin when the mouse button is moved inside the plugin iframe. |
| [MouseUpWindow](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/MouseUpWindow.md) | None | Sends an event to the plugin when the mouse button is released inside the plugin iframe. |
| [OnDropEvent](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/OnDropEvent.md) | None | Implements the external drag&drop emulation. |
| [OnEncryption](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/OnEncryption.md) | None | Encrypts the document. |
| [PasteHtml](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/PasteHtml.md) | None | Pastes text in the HTML format into the document. |
| [PasteText](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/PasteText.md) | None | Pastes text into the document. |
| [PutImageDataToSelection](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/PutImageDataToSelection.md) | None | Replaces the first selected drawing with the image specified in the parameters. |
| [RemovePlugin](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/RemovePlugin.md) | object | Removes a plugin with the specified GUID. |
| [ReplaceTextSmart](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/ReplaceTextSmart.md) | boolean | Replaces each paragraph (or text in cell) in the select with the corresponding text from an array of strings. |
| [SetFormValue](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/SetFormValue.md) | None | Sets a value to the specified form. |
| [SetMacros](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/SetMacros.md) | None | Sets macros to the document. |
| [SetPluginsOptions](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/SetPluginsOptions.md) | None | Configures plugins from an external source. The settings can be set for all plugins or for a specific plugin. |
| [SetProperties](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/SetProperties.md) | None | Sets the properties to the document. |
| [ShowButton](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/ShowButton.md) | None | Shows or hides buttons in the header. |
| [ShowError](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/ShowError.md) | None | Shows an error/warning message. |
| [ShowInputHelper](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/ShowInputHelper.md) | None | Shows the input helper. |
| [StartAction](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/StartAction.md) | None | Specifies the start action for long operations. |
| [UnShowInputHelper](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/UnShowInputHelper.md) | None | Unshows the input helper. |
| [UpdatePlugin](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/plugins/interacting-with-editors/form-api/Methods/UpdatePlugin.md) | object | Updates a plugin using the specified plugin config. |
