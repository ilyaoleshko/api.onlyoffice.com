# Changelog

The list of changes of ONLYOFFICE Docs API.

## Version 9.4

- Added the [plugin command logging](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/automation-api.md#command-logging) feature for enabling debug output of plugin commands in the browser console.
- Added the [editorConfig.plugins.disable](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/plugins.md#disable) parameter to block specific plugins on load.
- Added Croatian (`hr`) to the list of supported [interface languages](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor.md#lang).
- Removed the deprecated `editorConfig.customization.commentAuthorOnly` field.
- Added the `roles` parameter to the [onStartFilling](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onstartfilling) event with role and user information.
- Fixed a memory leak in the [destroyEditor](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#destroyeditor) method that prevented full cleanup.

## Version 9.1

- The document is opened in viewer mode with an error message if it cannot be [locked](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/key-concepts.md#lock) in WOPI.
- Added the [UserCanOnlyComment](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/wopi-rest-api/checkfileinfo.md#UserCanOnlyComment) property to the *CheckFileInfo* WOPI operation.
- The [editorConfig.customization.uitheme](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#uitheme) parameter is now available for the mobile editors.
- Added opening for [hml](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document.md#filetype) format.
- Added conversion from [pptx](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/conversion-tables.md#presentation-file-formats) format to *txt*.
- Changed the [editorConfig.customization.logo.image](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#logoimage) size requirement to 300x20.

## Version 9.0

- Added the [editorConfig.customization.suggestFeature](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#suggestfeature) parameter.
- Changed [editorConfig.customization.macros](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#macros): in version 9.0.3, this parameter completely disables running, adding, and editing macros (not just automatic startup).
- The [editorConfig.customization.toolbarHideFileName](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#toolbarhidefilename) parameter is now available for the mobile editors.
- Added the *theme-white* and *theme-night* theme ids to the [editorConfig.customization.uiTheme](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#uitheme) parameter.
- Added opening for [odg](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document.md#filetype) format.
- Added opening for [md](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document.md#filetype) format.
- Added the ability to [preload](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/get-started/configuration/preload.md) the editor static resources.
- Added the [editorConfig.customization.forceWesternFontSize](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#forcewesternfontsize) parameter for the Chinese (Simplified) UI.
- Added the [editorConfig.customization.layout.header.user](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-white-label.md#layoutheaderuser) parameter.
- Added conversion from [vsdm, vsdx, vssm, vssx, vstm, vstx](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/conversion-tables.md#diagram-document-file-formats) formats.
- Added the *diagram* document type to the [documentType](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config.md#documenttype) parameter.

## Version 8.3

- Added the [editorConfig.customization.features.featuresTips](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#featuresfeaturestips) parameter.
- Added the [editorConfig.customization.showHorizontalScroll](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#showhorizontalscroll) and [editorConfig.customization.showVerticalScroll](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#showverticalscroll) parameters.
- Added the [editorConfig.customization.slidePlayerBackground](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#slideplayerbackground) parameter.
- Added the [editorConfig.customization.wordHeadingsColor](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#wordheadingscolor) parameter.
- Added the [editorConfig.customization.mobile.info](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#mobileinfo) parameter.
- Added opening for [pages, key, numbers, hwp, hwpx](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document.md#filetype) formats.
- Added the [events.onUserActionRequired](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onuseractionrequired) event.
- Added the [refreshFile](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#refreshfile) method.
- Added the [events.onRequestRefreshFile](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestrefreshfile) event.
- Added the [events.onStartFilling](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onstartfilling) event.
- Added the *roles* parameter to the [events.onRequestStartFilling](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequeststartfilling) event.
- Added the [events.onRequestFillingStatus](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestfillingstatus) event.
- Added the [editorConfig.customization.startFillingForm](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#startfillingform) parameter.
- Added the *roles* field to the [editorConfig.user](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor.md#user).
- Added the [editorConfig.customization.mobile.disableForceDesktop](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#mobiledisableforcedesktop) parameter.
- The document editing will be prohibited for all users editing the document with the specified *key*, if the *users* parameter is not specified for the [drop](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service/drop.md) command.
- The [editorConfig.customization.submitForm](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#submitform) parameter can now be used as an object.
- The [editorConfig.customization.compactToolbar](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#compacttoolbar) parameter is now available for the viewer.
- Added the [editorConfig.customization.pointerMode](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#pointermode) parameter.
- The [editorConfig.customization.layout.toolbar.insert](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-white-label.md#layouttoolbarinsert) parameter can now be used as an object with the [file](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-white-label.md#layouttoolbarinsertfile) and [field](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-white-label.md#layouttoolbarinsertfield) fields.
- The [editorConfig.customization.layout.toolbar.layout](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-white-label.md#layouttoolbarlayout) parameter can now be used as an object with the [pagecolor](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-white-label.md#layouttoolbarlayoutpagecolor) field.

## Version 8.2

- The [editorConfig.customization.mobileForceView](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#mobileforceview) parameter is deprecated, please use the [editorConfig.customization.mobile](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#mobile) parameter instead.
- Added the *Password* and *PasswordToOpen* request parameters to the [WOPI conversion API](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/conversion-api.md).
- The [editorConfig.region](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor.md#region) field is now used to define the default measurement units in all editor types.
- The [editorConfig.location](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor.md#location) field is deprecated, please use the [editorConfig.region](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor.md#region) field instead.
- Added the *insert-text* type of document selection to the *c* parameter of the [setRequestedDocument](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setrequesteddocument) method.
- The `https://documentserver/coauthoring/CommandService.ashx` address of the [command service](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service.md) is replaced with `https://documentserver/command`.
- Added the *users* parameter to the response of the [info](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service/info.md) command.
- Added the [tabBackground](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#featurestabbackground) field to the *editorConfig.customization.features* parameter.
- Added the [tabStyle](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#featurestabstyle) field to the *editorConfig.customization.features* parameter.
- Added the [imageLight](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#logoimagelight) field to the *editorConfig.customization.logo* parameter.
- The [editorConfig.customization.toolbarNoTabs](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#toolbarnotabs) field is deprecated, please use the [editorConfig.customization.features.tabStyle](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#featurestabstyle) and [editorConfig.customization.features.tabBackground](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#featurestabbackground) fields instead.

## Version 8.1

- Added the [editorConfig.plugins.options](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/plugins.md#options) parameter.
- Added the possibility to [insert](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#insertimage) the *tif* / *tiff* image type into the file.
- Added the [startFilling](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#startfilling) method.
- Added the [events.onRequestStartFilling](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequeststartfilling) event.
- Added the [docs\_api\_config](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/host-page.md#parameters) parameter to the *form* element of the WOPI host page.
- Added the [pdf](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/request.md#pdf) field to the conversion request.
- Added the [events.onSubmit](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onsubmit) event.
- Added the [events.onSaveDocument](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onsavedocument) event.
- Added the *roles* field to the [editorConfig.customization.features](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#features) parameter.
- Added the [shardkey](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/get-started/configuration/shard-key.md) parameter to the URL query string when sending requests to the ONLYOFFICE Docs API, document command service, document conversion service, or document builder service.
- Added the [addContextMenuItem](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/automation-api/connector-class.md#addcontextmenuitem), [addToolbarMenuItem](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/automation-api/connector-class.md#addtoolbarmenuitem) and [updateContextMenuItem](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/automation-api/connector-class.md#updatecontextmenuitem) methods to the *Automation API*.
- Added the [-10 error code](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/error-codes.md) to the Conversion API.
- The [editorConfig.customization.logo](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#logo) parameter is now available for the mobile editors.
- Added the *visible* field to the [editorConfig.customization.logo](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#logo) parameter.
- Added the [formsubmit](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/wopi-discovery.md#formsubmit) action to the WOPI discovery.
- The [editorConfig.customization.goback.requestClose](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#goback) field is deprecated, please use the [editorConfig.customization.close](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#close) field instead.
- Added the [Save Copy As](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/wopi-rest-api/putrelativefile.md#save-copy-as) functionality to WOPI.
- Change the default value of the [editorConfig.customization.hideRightMenu](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#hiderightmenu) parameter to *true*.

## Version 8.0

- Added the [document.isForm](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document.md#isform) parameter.
- Added the [WOPISrc](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/key-concepts.md#wopisrc) query parameter to the requests from the browser to the server.
- Added the [watermark](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/request.md#watermark) field to the conversion request.
- Added the *pdf* document type to the [documentType](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config.md#documenttype) parameter.
- Added the [formsdataurl](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/callback-handler.md#formsdataurl) parameter to the *Callback handler*.
- Added the *data.id* parameter to the [events.onRequestUsers](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestusers) event.
- Added the *users.image* field to the [setUsers](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setusers) method.
- Added the *info* operation type to the [setUsers](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setusers) method and [events.onRequestUsers](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestusers) event.
- Added the *image* field to the [editorConfig.user](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor.md#user) parameter.
- Added the [editorConfig.customization.mobileForceView](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#mobileforceview) parameter.
- Added the *link* field to the *data* object which is sent to the [events.onRequestReferenceData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestreferencedata) event.

## Version 7.5

- Added the **3** type for the [forcesavetype](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/callback-handler.md#forcesavetype) parameter of the callback handler.
- Added the [editorConfig.customization.submitForm](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#submitform) parameter.
- The [events.onRequestMailMergeRecipients](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestmailmergerecipients) event is deprecated, please use the [events.onRequestSelectSpreadsheet](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestselectspreadsheet) event instead.
- The [setMailMergeRecipients](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setmailmergerecipients) method is deprecated, please use the [setRequestedSpreadsheet](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setrequestedspreadsheet) method instead.
- Added the [setReferenceSource](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setreferencesource) method.
- Added the [events.onRequestReferenceSource](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestreferencesource) event.
- Added the [-9 error code](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/error-codes.md) to the Conversion API.
- Added the *key* field to the [setReferenceData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setreferencedata) method.
- The [events.onRequestCompareFile](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestcomparefile) event is deprecated, please use the [events.onRequestSelectDocument](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestselectdocument) event instead.
- The [setRevisedFile](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setrevisedfile) method is deprecated, please use the [setRequestedDocument](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setrequesteddocument) method instead.
- Added the [events.onRequestOpen](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestopen) event.
- Added the [deleteForgotten](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service/deleteforgotten.md), [getForgotten](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service/getforgotten.md), and [getForgottenList](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service/getforgottenlist.md) commands.

## Version 7.4

- Added the [mobileView](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/wopi-discovery.md#mobileView) and [mobileEdit](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/wopi-discovery.md#mobileEdit) actions to the WOPI discovery.
- Added opening for [dps, dpt, et, ett, mhtml, stw, sxc, sxi, sxw, wps, wpt](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config.md#documenttype) formats.
- Added the *users.id* field to the [setUsers](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setusers) method.
- Added the *c* parameter to the [setUsers](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setusers) method and [events.onRequestUsers](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestusers) event.

## Version 7.3

- Added the WOPI [Conversion API](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/conversion-api.md).
- Added the [setReferenceData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setreferencedata) method.
- Added the [events.onRequestReferenceData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestreferencedata) event.
- Added the [document.referenceData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document.md#referencedata) parameter.
- Added the [UserCanNotWriteRelative](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/wopi-rest-api/checkfileinfo.md#UserCanNotWriteRelative) property to the *CheckFileInfo* WOPI operation.
- Added a scheme for [editing binary document formats](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/editing-binary-documents.md).
- Added the [convert](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/wopi-discovery.md#convert) action to the WOPI discovery.
- Added the [PutRelativeFile](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/wopi-rest-api/putrelativefile.md) WOPI operation.

## Version 7.2

- Added the [title](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config.md#title) parameter.
- Added the [editorConfig.customization.integrationMode](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#integrationmode) parameter.
- Added the [Connector](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/automation-api/connector-class.md) class to interact with documents, spreadsheets, presentations, PDFs, and fillable forms from the outside.
- Added the *theme-contrast-dark* theme id to the [editorConfig.customization.uiTheme](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#uitheme) parameter.
- Added the *phone* field to the [editorConfig.customization.customer](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#customer) parameter.
- Added the [connections\_view](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service/license.md#license.connections_view), [users\_view\_count](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service/license.md#license.users_view_count) and [users\_view](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service/license.md#quota.users_view) parameters to the license response.
- Added the [live viewer](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/get-started/how-it-works/viewing.md) mode to the document, spreadsheet and presentation editors.
- Added the [embedview](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/wopi-discovery.md#embedview) action to the WOPI discovery.
- The [services.CoAuthoring.secret.browser.string](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/signature.md#configuration-parameters) parameter is deprecated, please use the [services.CoAuthoring.secret.inbox.string](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/signature.md#configuration-parameters) parameter instead.

## Version 7.1

- The *services.CoAuthoring.token.inbox.inBody* and *services.CoAuthoring.token.outbox.inBody* parameters for enabling [token in body](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/signature/request/token-in-body.md) are deprecated.
- Added the *X-LOOL-WOPI-IsModifiedByUser*, *X-LOOL-WOPI-IsAutosave* and *X-LOOL-WOPI-IsExitSave* request headers to the [PutFile](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/wopi-rest-api/putfile.md) WOPI operation to distinguish between the type of document saving.
- The [editorConfig.customization.chat](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#chat) parameter is deprecated, please use the [document.permissions.chat](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document/permissions.md#chat) parameter instead.
- Added conversion from [dps, dpt, et, ett, htm, mhtml, stw, sxc, sxi, sxw, wps, wpt, xlsb, xml](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/conversion-tables.md) format.
- Added opening for [xlsb](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config.md#documenttype) format.
- The parameter list in the initialization config [signature](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/signature/browser.md#opening-file) has become strictly regulated.
- The [editorConfig.customization.spellcheck](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#spellcheck) field is deprecated, please use the [editorConfig.customization.features.spellcheck](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#features) field instead.
- Added the [editorConfig.customization.features](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#features) parameter section.
- Added the [documentLayout](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/request.md#documentLayout) parameter to the conversion request.
- Added the [documentRenderer](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/request.md#documentRenderer) parameter to the conversion request.
- Added conversion from [pdf/xps/oxps](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/conversion-tables.md#document-file-formats) formats to *docx*.
- Added the [document.permissions.userInfoGroups](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document/permissions.md#userinfogroups) parameter.
- Added conversion from [djvu](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/conversion-tables.md#document-file-formats) format to *pdf*.
- Added conversion to [ppsm, ppsx](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/conversion-tables.md#presentation-file-formats) formats.

## Version 7.0

- The [callbackUrl](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/callback-handler.md) is used from the last tab of the same user.
- Added the *logoDark* field to the [editorConfig.customization.customer](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#customer) parameter.
- Added the *imageDark* field to the [editorConfig.customization.logo](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#logo) parameter.
- The *imageEmbedded* field of the [editorConfig.customization.logo](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#logo) parameter is deprecated, please use the *image* field instead.
- Added a signature to the request for file changes specified with the *changesUrl* parameter of the [setHistoryData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#sethistorydata) method.
- Added the [document.permissions.protect](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document/permissions.md#protect) field.
- Added the *fileType* parameter to the [onDownloadAs](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#ondownloadas), [onRequestRestore](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestrestore) and [onRequestSaveAs](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestsaveas) events.
- Added the possibility to insert several images via the [insertImage](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#insertimage) method.
- The [assemblyFormatAsOrigin](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/get-started/how-it-works/saving-file.md#saving-in-original-format) server setting is enabled by default.
- Added the *ooxml* and *odf* values to the [outputtype](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/request.md#outputtype) parameter of the conversion request.
- Added the *fileType* and *previous.fileType* parameters to the [setHistoryData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#sethistorydata) method.
- Added the [filetype](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/callback-handler.md#filetype) parameter to the *Callback handler*.
- Added the [fileType](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/response.md#fileType) field to the conversion response.
- Added conversion to [docm, dotm, xlsm, xltm, pptm, potm](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/conversion-tables.md) formats.
- The [editorConfig.customization.reviewDisplay](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#reviewdisplay), [editorConfig.customization.showReviewChanges](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#showreviewchanges), [editorConfig.customization.trackChanges](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#trackchanges) parameters are deprecated, please use the [editorConfig.customization.review](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#review) parameter instead.
- Added the [editorConfig.customization.review.hideReviewDisplay](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#review) field.
- Added the [editorConfig.customization.review.hoverMode](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#review) field.
- Added the possibility to view the [document history](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/get-started/how-it-works/document-history.md) of the spreadsheet files.
- Added the [UI\_InsertGraphic](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/postmessage.md#UI_InsertGraphic) message for the PostMessage WOPI protocol.

## Version 6.4

- Added opening for [oxps](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config.md#documenttype) format.
- Added support for [WOPI protocol](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/using-wopi/overview.md).
- Added the [editorConfig.wopi](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor.md#wopi) section.
- Added the *simple* value to the [editorConfig.customization.reviewDisplay](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#reviewdisplay) parameter.
- Added the [threaded comments](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/get-started/how-it-works/commenting.md#threaded-comments-in-spreadsheets) saving in the spreadsheet files.
- Added the [editorConfig.customization.uiTheme](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#uitheme) field.
- Added the possibility to view the [document history](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/get-started/how-it-works/document-history.md) for the presentation files.
- Added the [editorConfig.customization.hideNotes](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#hidenotes) field.
- Added the [editorConfig.coEditing](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor.md#coediting) field.
- Added the [requestClose](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#requestclose) method.
- Added the [document.permissions.commentGroups](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document/permissions.md#commentgroups) field.
- Added the [events.onPluginsReady](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onpluginsready) event.

## Version 6.3

- Added the [license](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service/license.md) command.
- Added the [editorConfig.customization.hideRulers](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#hiderulers) field.
- Added the [editorConfig.customization.anonymous](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#anonymous) field.
- The `editorConfig.customization.commentAuthorOnly` field is deprecated, please use the [document.permissions.editCommentAuthorOnly](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document/permissions.md#editcommentauthoronly) and [document.permissions.deleteCommentAuthorOnly](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document/permissions.md#deletecommentauthoronly) fields.
- Added the [setFavorite](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setfavorite) method.
- Added the *data.favorite* parameter to the [events.onMetaChange](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onmetachange) event.
- Added the [document.info.favorite](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document/info.md#favorite) field.
- Added the [document.permissions.reviewGroups](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document/permissions.md#reviewgroups) field.
- Added conversion to [epub, fb2, html](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/conversion-tables.md#document-file-formats) formats.
- Added conversion from [xml](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/conversion-tables.md#document-file-formats) format.
- Removed the deprecated `document.info.author` parameter.
- Removed the deprecated `document.info.created` parameter.

## Version 6.2

- Added a new [actions.type](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/callback-handler.md#actions) field value (*actions.type = 2*).
- Added the [editorConfig.customization.trackChanges](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#trackchanges) field.
- Added the [editorConfig.customization.toolbarHideFileName](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#toolbarhidefilename) field.
- The *callbackUrl* for *status* **6** is selected based on [forcesavetype](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/callback-handler.md).
- Added opening for [fb2](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config.md#documenttype) format.

## Version 6.1

- The *text*, *spreadsheet* and *presentation* values for [documentType](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config.md#documenttype) parameter is deprecated, please use *word*, *cell* and *slide* values instead.
- Added the *group* field to the [editorConfig.user](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor.md#user).
- Added the [editorConfig.customization.reviewPermissions](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#reviewpermissions) parameter.
- Added conversion from [fb2](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/conversion-tables.md#document-file-formats) format.
- Removed the deprecated `document.permissions.changeHistory` parameter.
- Removed the deprecated `document.permissions.rename` parameter.

## Version 6.0

- Added the type of insertion in [events.onRequestInsertImage](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestinsertimage) event.
- Added the [editorConfig.templates](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor.md#templates) field.
- Added the [editorConfig.customization.plugins](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#plugins) field.
- Added the [editorConfig.customization.macros](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#macros) field.
- Added the [editorConfig.customization.macrosMode](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#macrosmode) field.
- Added the [events.onRequestCreateNew](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestcreatenew) event.
- Added the [document.permissions.copy](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document/permissions.md#copy) field.
- The `document.permissions.rename` field is deprecated, please add the [events.onRequestRename](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestrename) field instead.

## Version 5.5

- The `https://documentserver/ConvertService.ashx` address of the [conversion service](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/request.md) is replaced with `https://documentserver/converter`.
- Added the [editorConfig.customization.spellcheck](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#spellcheck) field.
- Added conversion to [pdfa](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/conversion-tables.md#document-file-formats) format.
- Added the [events.onRequestCompareFile](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestcomparefile) event.
- Added the [setRevisedFile](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setrevisedfile) method.
- Token in [methods](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/signature/browser.md#methods) parameters.
- The `document.permissions.changeHistory` field is deprecated, please add the [events.onRequestRestore](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestrestore) field instead.
- Added the [editorConfig.customization.goback.requestClose](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#goback) field.
- Added the [events.onRequestSharingSettings](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestsharingsettings) event.
- Added the [editorConfig.customization.unit](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#unit) field.
- Added the [region](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/request.md#region) field.
- Added the [spreadsheetLayout](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/request.md#spreadsheetLayout) field.
- Added [input error](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/error-codes.md) for conversion.
- The [events.onRequestSendNotify](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestsendnotify) event and the [events.onRequestUsers](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestusers) event can be set independently.
- Added the [editorConfig.customization.mentionShare](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#mentionshare) field.
- The *callbackUrl* is selected based on [status](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/callback-handler.md).
- Added the [editorConfig.customization.compatibleFeatures](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#compatiblefeatures) field.

## Version 5.4

- Added the [editorConfig.region](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor.md#region) field.
- The `document.info.created` field is deprecated, please use the [document.info.uploaded](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document/info.md#uploaded) field instead.
- The `document.info.author` field is deprecated, please use the [document.info.owner](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document/info.md#owner) field instead.
- The `events.onReady` event is removed.
- The `firstname` and `lastname` fields in the [editorConfig.user](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor.md#user) object are removed.
- Added the [events.onRequestSaveAs](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestsaveas) event.
- Added the [events.onRequestInsertImage](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestinsertimage) event.
- Added the [insertImage](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#insertimage) method.
- Added the [events.onRequestMailMergeRecipients](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestmailmergerecipients) event.
- Added the [setMailMergeRecipients](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setmailmergerecipients) method.
- Added the [setSharingSettings](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setsharingsettings) method.
- Added the [events.onRequestUsers](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestusers) event.
- Added the [setUsers](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setusers) method.
- Added the [events.onRequestSendNotify](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestsendnotify) event.

## Version 5.3

- Added [conversion](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/conversion-tables.md) to the OOXML (dotx, xltx, potx) and ODF (ott, ots, otp) templates.
- Added the [editorConfig.customization.reviewDisplay](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#reviewdisplay) field.
- The `editorConfig.customization.commentAuthorOnly` field is now used to restrict comment deletion as well.
- Added the [editorConfig.customization.compactHeader](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#compactheader) field.
- Added the [editorConfig.customization.hideRightMenu](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#hiderightmenu) field.
- Added the [editorConfig.customization.toolbarNoTabs](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#toolbarnotabs) field.
- Added [conversion error](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/error-codes.md) for password protected documents.
- Added the [editorConfig.actionLink](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor.md#actionlink) field.
- Added the [setActionLink](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setactionlink) method.
- Added the [events.onMakeActionLink](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onmakeactionlink) event.

## Version 5.2

- Token in request [body](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/signature/request/token-in-body.md) parameters.
- [document.permissions.comment](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document/permissions.md#comment) is available in all types of editors.
- Added the [document.permissions.fillForms](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document/permissions.md#fillforms) field.
- Added the [editorConfig.customization.help](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#help) field.
- Added the possibility to make the [editorConfig.customization.logo](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#logo) not clickable.
- Added for the [aspect](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/request.md#thumbnail.aspect) field value *2* for the conversion.

## Version 5.1

- Added the *format* parameter to the [downloadAs](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#downloadas) method.
- Added the [document.permissions.modifyContentControl](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document/permissions.md#modifycontentcontrol) field.
- Added conversion for [OpenDocument Template](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/conversion-tables.md) formats.
- Added the [events.onRequestClose](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestclose) event.
- Added the [editorConfig.customization.goback.blank](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#goback) field.

## Version 5.0

- Added the [document.permissions.modifyFilter](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document/permissions.md#modifyfilter) field.
- Added conversion for macro-enabled document, document template and flat document [formats](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/conversion-tables.md).
- The `events.onReady` event is deprecated, please use the [events.onAppReady](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onappready) event instead.
- Added the [events.onDocumentReady](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#ondocumentready) event.
- Added the [editorConfig.plugins.autostart](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/plugins.md#autostart) field.
- Added the [events.onWarning](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onwarning) event.
- Added the [Document Builder service](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/document-builder-api.md).

## Version 4.4

- Changed the [showMessage](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#showmessage) method.
- Added conversion to [odp](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/conversion-tables.md#presentation-file-formats) format.
- Added the [document.permissions.comment](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/document/permissions.md#comment) field.
- Added the `document.permissions.changeHistory` field.
- Added the [events.onRequestRestore](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestrestore) event.
- Added the `document.permissions.rename` field.
- Added the [events.onRequestRename](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestrename) event.
- Added the [meta](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service/meta.md) command.
- Added the [events.onMetaChange](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onmetachange) event.
- Changed the use of *callbackUrl* from the [last user](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/callback-handler.md) who joined the co-editing.
- Added the [editorConfig.location](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor.md#location) field.
- Added the [editorConfig.embedded.autostart](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/embedded.md#autostart) field.

## Version 4.3

- Added the [destroyEditor](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#destroyeditor) method.
- Removed the `editorConfig.plugins.url` field from the plugin connection pattern.
- Added the `editorConfig.customization.commentAuthorOnly` field.
- Added the [editorConfig.customization.forcesave](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#forcesave) field.
- Added the [editorConfig.customization.showReviewChanges](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#showreviewchanges) field.
- Added the [forcesavetype](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/callback-handler.md#forcesavetype) field in the callback handler request when force saving the file.
- Added the [JSON format for response](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/response.md) from document conversion service.

## Version 4.2

- The `firstname` and `lastname` fields are deprecated, please use the [name](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor.md#username) field instead.
- Added the possibility to specify the values for the [editorConfig.customization.chat](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#chat) and [editorConfig.customization.comments](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#comments) in the Open Source version.
- Added the [editorConfig.customization.compactToolbar](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#compacttoolbar) field.
- Added the [editorConfig.customization.zoom](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#zoom) field.
- Added the [editorConfig.customization.autosave](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/editor/customization/customization-standard-branding.md#autosave) field.
- The [changeshistory](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/callback-handler.md#changeshistory) field is removed, please use the [history](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/callback-handler.md#history) field instead.
- Changed the [setHistoryData](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#sethistorydata) method.
- Added the possibility to convert files to [thumbnail](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/request.md#generating-png-thumbnail-from-docx) in the [document conversion service](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/request.md).
- The POST requests are now used for the interaction with the [document command service](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service.md) and the [document conversion service](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/conversion-api/request.md).
- Added the [version](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service/version.md) command.
- Added the [signature](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/signature.md) for the editor opening and for the incoming and outgoing requests.
