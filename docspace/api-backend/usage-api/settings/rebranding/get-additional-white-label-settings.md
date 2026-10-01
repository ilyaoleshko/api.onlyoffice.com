# getAdditionalWhiteLabelSettings

> AdditionalWhiteLabelSettingsDtoWrapper getAdditionalWhiteLabelSettings()

`GET /api/2.0/settings/rebranding/additional`

Get the additional white label settings

Returns which of the ONLYOFFICE help and community resources the interface may offer - the sample documents, the Help Center link, the Feedback and Support link, the user forum, the video guides and the license agreements - so a client can hide the entries that are switched off. Any authenticated user may call it; no administrator permission is required, and a portal whose payment has lapsed is served as well. The call is read-only and idempotent. Each flag is `true` when the entry may be shown and `false` when it must be hidden, and `isDefault` tells whether the whole set is still the built-in one. The flags are installation-wide, so every portal of a server installation reports the same ones. They say nothing about the caller's own permissions, and the addresses behind the entries are not part of the answer. Change the flags with `POST api/2.0/settings/rebranding/additional` and reset them with `DELETE api/2.0/settings/rebranding/additional`.

## Parameters
This endpoint does not need any parameter.

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The help and community resources the interface may offer, with the default flag | [**AdditionalWhiteLabelSettingsDtoWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/additional-white-label-settings-dto-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**AdditionalWhiteLabelSettingsDtoWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/additional-white-label-settings-dto-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#openid)

## HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
