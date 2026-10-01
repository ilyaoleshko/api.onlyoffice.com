---
sidebar_position: -2
---

# Renaming

## How to rename the created document?

Please see the [Renaming file](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/get-started/how-it-works/renaming-file.md) section to find out how file renaming works in ONLYOFFICE Docs and what is needed to rename the created document.

## How to update the name of the document for all collaborative editors?

To do that the [meta](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service/meta.md) command is available. The request must be sent to the [document command service](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/docs-api/additional-api/command-service.md), using the `meta` value for the `c` parameter:

  ``` json
  {
    "c": "meta",
    "key": "Khirz6zTPdfd7",
    "meta": {
      "title": "Example Document Title.docx"
    }
  }
  ```
