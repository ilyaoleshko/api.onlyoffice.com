# createFile

> FileIntegerWrapper createFile(folderId, CreateFileJsonElement)

`POST /api/2.0/files/{folderId}/file`

Create a file

Creates a file in the folder named in the route and answers with the stored file. The extension in the title decides the format: an extension of a known text, spreadsheet or presentation format is rewritten to the portal's own DOCX, XLSX or PPTX, a title with no extension at all gets DOCX added, while an unknown extension and the few formats the portal keeps as they are stay untouched; `enableExternalExt=true` stores the title verbatim and skips that rewriting. The content comes from one of three sources, tried in this order: `formId` copies a ready form out of the form gallery, `templateId` copies an existing file the caller can read - a number for a file in the portal, a string for one in a connected third-party storage - and with neither of them the portal's blank template for that format and the caller's language is used. The caller needs the right to create files in the folder, and the room roots, Archive and the template sections are refused even to an admin. The call is mutating and not idempotent. To create the file in the caller's own section use `POST api/2.0/files/@my/file`.

## Parameters

|Name | In | Type | Description | Notes |
|------------- | ------------- | ------------- | ------------- | -------------|
| **folderId** | path | **Integer** (int32) | The folder the file is created in. | [required] [example: `1`] |
| **CreateFileJsonElement** | body | [**CreateFileJsonElement**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/create-file-json-element.md) | The title of the new file and the source of its content. | [required] |

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The file created in the folder: its id and the title the portal actually stored, whose extension may differ from the requested one; `thumbnailStatus` says whether the preview is already built | [**FileIntegerWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/file-integer-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **400** | Bad Request. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**FileIntegerWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/file-integer-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#openid)

## HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json
