# getLoginSettings

> LoginSettingsWrapper getLoginSettings()

`GET /api/2.0/settings/security/loginsettings`

Get login settings

Returns the brute-force protection of the sign-in form for the current portal: how many failed attempts are tolerated, how long the window they are counted in lasts, and how long an offender stays blocked. The caller needs the portal-settings right of a DocSpace administrator; members without it are refused, and anonymous callers are not admitted. The operation is read-only and honours `If-Modified-Since`: send back the `Last-Modified` value of an earlier answer and unchanged settings come back as an empty not-modified response rather than a body. `checkPeriod` and `blockTime` are counted in seconds. A portal nobody has configured tolerates 5 failed attempts inside a window of 60 seconds and blocks for 60 seconds, and reports `isDefault` true; the flag turns false as soon as any of the three values differs from that. The answer describes the portal-wide policy only: it does not say which accounts or addresses are blocked at the moment, while a lockout that has already happened is recorded in the login history and can be read with `GET api/2.0/security/audit/login/filter`. Change the numbers with `PUT api/2.0/settings/security/loginsettings`, or put them back with `DELETE api/2.0/settings/security/loginsettings`.

## Parameters
This endpoint does not need any parameter.

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The brute-force protection settings of the portal: the tolerated attempts, the counting window and the block in seconds, and whether they match the shipped defaults | [**LoginSettingsWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/login-settings-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**LoginSettingsWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/login-settings-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#openid)

## HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
