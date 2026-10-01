# setFilesOrder

> FileEntryIntegerArrayWrapper setFilesOrder(OrdersRequestDtoInteger)

`PUT /api/2.0/files/order`

Set order of files

Puts several files and folders at given positions in one go and answers with the entries that were moved, each with the position it now holds. Every item of `items` names an entry by its identifier and its kind - a file or a folder - and the position it is to take, counting from 1; a position may also be sent as a dotted path, as in 1.2.3, of which only the last segment is read. The items are applied one after another in the order they are sent, and each of them shifts its neighbours, so the result depends on that order; the whole request is not one transaction, and a failure in the middle leaves the items before it moved. Every item has to lie in a room the caller may administer, which the room admin and a DocSpace admin acting as room manager do: read-only access, a guest and an anonymous caller are refused, and an identifier that matches nothing is answered as not found. Ordering only means something in rooms whose contents are indexed. The call is mutating. For a single file use `PUT api/2.0/files/{fileId}/order`.

## Parameters

|Name | In | Type | Description | Notes |
|------------- | ------------- | ------------- | ------------- | -------------|
| **OrdersRequestDtoInteger** | body | [**OrdersRequestDtoInteger**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/orders-request-dto-integer.md) |  | [optional] |

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The files and folders that were moved, with the positions they now hold | [**FileEntryIntegerArrayWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/file-entry-integer-array-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **400** | Bad Request. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**FileEntryIntegerArrayWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/file-entry-integer-array-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#openid)

## HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json
