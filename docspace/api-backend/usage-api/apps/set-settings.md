# setSettings

> AppWrapper setSettings(id, SetAppSettingsBody)

`PUT /api/2.0/apps/{id}/settings`

Save app settings

Stores the application-specific settings document of one portal application for the current portal. The identifier must be an application declared in the installation configuration, as listed by `GET api/2.0/apps`. The caller must be a portal administrator allowed to edit the portal settings. The call is mutating and idempotent, and it replaces the whole document instead of merging into it: read the current one with `GET api/2.0/apps/{id}/settings`, change it and send it back complete, or send `null` to drop the saved document and let the application fall back to its own defaults. Any valid JSON value is accepted, since the content is stored as it is and is interpreted by the application rather than by the portal, while a body that is not valid JSON fails with 400 and stores nothing. The response is the application in its new state, with the stored document echoed back. Unlike `PUT api/2.0/apps/{id}/enabled`, this operation sends no notification to the connected clients, which pick the new settings up on their next read.

## Parameters

|Name | In | Type | Description | Notes |
|------------- | ------------- | ------------- | ------------- | -------------|
| **id** | path | **String** | The application whose configuration is stored, by the identifier `GET api/2.0/apps` reports. An identifier not declared in the installation configuration answers 404. | [required] [example: `ai-room`] |
| **SetAppSettingsBody** | body | [**SetAppSettingsBody**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/set-app-settings-body.md) | The configuration to store for this portal, replacing whatever was stored before. | [required] |

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The application in its new state, with the stored settings document | [**AppWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/app-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **400** | The request body is not a valid JSON document, so no settings are stored | - | - |
| **403** | The caller is not allowed to edit the portal settings | - | - |
| **404** | No application with this identifier is configured on this installation | - | - |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**AppWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/app-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/apps.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/apps.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/apps.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/apps.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/apps.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/apps.md#openid)

## HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json
