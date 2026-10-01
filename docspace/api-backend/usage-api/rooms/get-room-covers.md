# getRoomCovers

> CoversResultArrayWrapper getRoomCovers()

`GET /api/2.0/files/rooms/covers`

Get room cover gallery

Returns the gallery of cover pictures a room can be given: every entry pairs the identifier to send to `POST api/2.0/files/rooms/{id}/cover` with the drawing itself as inline vector markup ready to be rendered. The gallery is built into the product rather than stored per portal, so it is the same for every account and every room, does not depend on what rooms exist, and its identifiers do not change with the language of the request. The identifiers are unique and stable, which makes them safe to keep in a client, while the drawings behind them may change between product versions. Any account of the portal may read the gallery, but a guest is refused. The list is the only source of valid cover identifiers: a value that is not in it is rejected wherever a cover is set, including room creation and room update. The call changes nothing and is safe to repeat.

## Parameters
This endpoint does not need any parameter.

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The built-in room covers with their identifiers and vector markup | [**CoversResultArrayWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/covers-result-array-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**CoversResultArrayWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/covers-result-array-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#openid)

## HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
