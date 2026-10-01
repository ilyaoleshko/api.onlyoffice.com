---
sidebar_position: -16
---

# Renaming file

The figure and steps below explain how a document is renamed in ONLYOFFICE Docs.

![Renaming File](https://ilyaoleshko.github.io/assets/images/editor/rename.svg)

1. The user selects *Rename...* in the **document editor**.
2. The **document editor** sends the new name to the **document manager** via the [onRequestRename](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestrename) event.
3. The **document manager** sends the new name to the **document storage service**, where the integrator renames the file.
4. The **document storage service** sends a [meta](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service/meta.md) command to the **document command service** to update the document name.
5. The **document editing service** sends the new name to each user's **document editor** via the [onMetaChange](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onmetachange) event, making it visible to all users.

## How this can be done in practice

1. Create an `.html` file to [open the document](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/get-started/how-it-works/opening-file.md#how-this-can-be-done-in-practice).

2. In the editor initialization config, define the [onRequestRename](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestrename) event handler. When the user selects *Rename...* in the editor menu, this event fires with the new name (without the file extension) in `event.data`. In the handler, send the new name to your server so it can rename the file in the **document storage service**.

   ![onRequestRename](https://ilyaoleshko.github.io/assets/images/editor/onRequestRename.png#gh-light-mode-only)![onRequestRename](https://ilyaoleshko.github.io/assets/images/editor/onRequestRename.dark.png#gh-dark-mode-only)

   ``` ts
   function onRequestRename(event) {
     const newTitle = event.data;
     RENAME_FILE(newTitle);
   }
   
   const config = {
     events: {
       onRequestRename,
     },
   };

   const docEditor = new DocsAPI.DocEditor("placeholder", config);
   ```

   `RENAME_FILE` is a placeholder for your server-side logic that renames the document in the **document storage service**.

3. After renaming the file, send a request from your server to the [document command service](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service.md) with the [meta](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service/meta.md) command to update the name for all users editing the document:

   ``` json
   {
     "c": "meta",
     "key": "Khirz6zTPdfd7",
     "meta": {
       "title": "Example Document Title.docx"
     }
   }
   ```

4. When the [meta](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service/meta.md) command is received, the [onMetaChange](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onmetachange) event fires in each user's **document editor**. The new name is passed in `event.data.title`.

   ``` ts
   function onMetaChange(event) {
     const title = event.data.title;
   }
   
   const config = {
     events: {
       onMetaChange,
     },
   };

   const docEditor = new DocsAPI.DocEditor("placeholder", config);
   ```
