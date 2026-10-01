# createRoomTemplate

> RoomTemplateStatusWrapper createRoomTemplate(RoomTemplateDto)

`POST /api/2.0/files/roomtemplate`

Create a room template

Queues a background job that turns an existing room into a reusable room template, and returns the state of that job right away. The template lands in the portal's Templates section, inherits the source room's type, privacy, indexing, storage limit, lifetime, download and watermark settings, and receives copies of the room's files together with its ordinary subfolders and everything inside them; the service subfolders a room keeps for its own workflows are left out. The caller needs room-manager rights on the source room, and the room must not be archived: a room that cannot be found under Rooms is answered as missing, and every other refusal comes back as a rejection. The template is not ready when the response arrives, so poll `GET api/2.0/files/roomtemplate/status` until `isCompleted` is true, then read `templateId`; a non-empty `error` there means the job failed and the half-built template was removed. Only one template creation is tracked per caller, and starting another replaces the previous record. Setting `public` to true discards `share` and `groups` and shares the finished template with everyone instead, while `copyLogo` reuses the source room's own picture and makes `logo` irrelevant.

## Parameters

|Name | In | Type | Description | Notes |
|------------- | ------------- | ------------- | ------------- | -------------|
| **RoomTemplateDto** | body | [**RoomTemplateDto**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/room-template-dto.md) |  | [optional] |

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The state of the template creation just queued: `isCompleted` is still false, so the job has to be polled for its result | [**RoomTemplateStatusWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/room-template-status-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **400** | Bad Request. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**RoomTemplateStatusWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/room-template-status-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#openid)

## HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json
