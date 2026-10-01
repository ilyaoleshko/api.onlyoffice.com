---
sidebar_position: -9
---

# Comparing documents

Document comparison highlights the differences between two documents as tracked changes — the user can then accept or reject each one.

The figure and steps below explain the comparison flow.

![Comparing documents](https://ilyaoleshko.github.io/assets/images/editor/compare.png)

1. Using the **document manager** in the browser, the user opens a document to view or edit it.
2. The **document manager** initializes the **document editor** with a [`config`](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config.md) that includes the [`onRequestSelectDocument`](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestselectdocument) event handler.
3. The file is [opened](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/get-started/how-it-works/opening-file.md) for editing.
4. The user clicks **Document from Storage** in the Compare menu. The **document editor** fires the [`onRequestSelectDocument`](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestselectdocument) event with `data.c` set to `"compare"`.
5. The **document manager** lets the user select a comparison document from storage.
6. The **document manager** calls [`setRequestedDocument`](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setrequesteddocument) with the selected document's URL and `c: "compare"` to pass it to the **document editor** for comparison.

## How this can be done in practice

1. Create an `.html` file to [open the document](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/get-started/how-it-works/opening-file.md#how-this-can-be-done-in-practice).

2. Add the [`onRequestSelectDocument`](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/config/events.md#onrequestselectdocument) event handler to the editor config. When the user clicks **Document from Storage** in the Compare menu, this event fires with `data.c` set to `"compare"`. The handler calls [`setRequestedDocument`](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/usage-api/methods.md#setrequesteddocument) with the comparison document:

   ![onRequestSelectDocument](https://ilyaoleshko.github.io/assets/images/editor/onRequestSelectDocument.png#gh-light-mode-only)![onRequestSelectDocument](https://ilyaoleshko.github.io/assets/images/editor/onRequestSelectDocument.dark.png#gh-dark-mode-only)

   ``` ts
   const docEditor = new DocsAPI.DocEditor("placeholder", {
     events: {
       onRequestSelectDocument(event) {
         docEditor.setRequestedDocument({
           c: event.data.c,
           fileType: "docx",
           token: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJmaWxlVHlwZSI6ImRvY3giLCJ1cmwiOiJodHRwczovL2V4YW1wbGUuY29tL3VybC10by1leGFtcGxlLWRvY3VtZW50LmRvY3gifQ.t8660n_GmxJIppxcwkr_mUxmXYtE8cg-jF2cTLMtuk8",
           url: "https://example.com/url-to-example-document.docx",
         });
       },
     },
   });
   ```

   :::warning
   The `token` must be signed with your document server's JWT secret — the example token above is signed with a throwaway secret and will not validate on your server. Regenerate it whenever the parameters change. See [security](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/get-started/how-it-works/security.md) for details.
   :::

3. After the comparison loads, the user can accept or reject changes using the corresponding buttons on the top toolbar.

   ![Accept changes](https://ilyaoleshko.github.io/assets/images/editor/compare-documents.png#gh-light-mode-only)![Accept changes](https://ilyaoleshko.github.io/assets/images/editor/compare-documents.dark.png#gh-dark-mode-only)

When the user is done reviewing, the document is [saved](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/get-started/how-it-works/saving-file.md) with the accepted changes.
