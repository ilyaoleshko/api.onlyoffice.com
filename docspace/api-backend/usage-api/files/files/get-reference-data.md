# getReferenceData

> FileReferenceWrapper getReferenceData(GetReferenceDataDtoInteger)

`POST /api/2.0/files/file/referencedata`

Resolve a spreadsheet reference

Resolves a reference that a formula in one spreadsheet makes to another document, and answers with the descriptor the document service needs in order to read it: the title, the download address, the file type, the document key of the co-editing session, the web editor link and the signature token. Three ways of naming the target are tried in order, and the first that resolves wins: `fileKey` as a file id inside the portal named by `instanceId`, then `path` looked up among the files sitting next to `sourceFileId`, then `link`, short links included, from which the file id is read out. A link that points outside this portal is not resolved at all and comes back unchanged as the address to follow. The caller needs read access to the source file and to its folder, otherwise the call is refused. The call only reads. A reference that resolves to nothing is still answered with 200, with the error text filled in and the rest of the descriptor empty, so read the error before using any other field.

## Parameters

|Name | In | Type | Description | Notes |
|------------- | ------------- | ------------- | ------------- | -------------|
| **GetReferenceDataDtoInteger** | body | [**GetReferenceDataDtoInteger**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/get-reference-data-dto-integer.md) |  | [optional] |

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The reference descriptor, or the same object with the error text set when nothing resolved | [**FileReferenceWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/file-reference-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **400** | Bad Request. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**FileReferenceWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/file-reference-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#openid)

## HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json
