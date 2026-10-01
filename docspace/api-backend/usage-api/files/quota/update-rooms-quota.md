# updateRoomsQuota

> FolderIntegerArrayWrapper updateRoomsQuota(UpdateRoomsQuotaRequestDtoInteger)

`PUT /api/2.0/files/rooms/roomquota`

Change the room quota limit

Sets the same custom storage limit, in bytes, on every listed room and streams the updated rooms back in the order they were given. The per-room quota feature has to be on for the portal, and the value must stay within the portal own limit, otherwise the call is refused before anything is written. The caller must be a manager of each listed room, and an archived room or a room in the trash is refused. The list is not transactional: rooms processed before the offending one keep their new limit, so a failed call has to be checked room by room. Only numeric room ids are processed, which means ids of rooms stored in a connected third-party account are silently skipped. A room whose limit already equals the requested value is left untouched and still returned. To go back to the portal default use `PUT api/2.0/files/rooms/resetquota`, and to drop the custom limit entirely send a quota of -1 to `PUT api/2.0/files/rooms/{id}`.

## Parameters

|Name | In | Type | Description | Notes |
|------------- | ------------- | ------------- | ------------- | -------------|
| **UpdateRoomsQuotaRequestDtoInteger** | body | [**UpdateRoomsQuotaRequestDtoInteger**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/update-rooms-quota-request-dto-integer.md) |  | [optional] |

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The rooms as they are after the new limit was applied | [**FolderIntegerArrayWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/folder-integer-array-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **400** | Bad Request. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**FolderIntegerArrayWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/folder-integer-array-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#openid)

## HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json
