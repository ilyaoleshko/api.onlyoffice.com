# updateTfaAppCodes

> TfaAppCodeArrayWrapper updateTfaAppCodes()

`PUT /api/2.0/settings/tfaappnewcodes`

Regenerate the TFA backup codes

Replaces the current user's one-time backup codes with a freshly generated set and returns it. Use it once the previous codes have been spent or may have leaked: the whole old set stops being accepted the moment this call succeeds, so store the new codes before leaving the response. Any authenticated member may call it, always for their own account. The authenticator method has to be enabled on the portal and an application has to be linked to the account already, otherwise the call answers 405, and accounts flagged as outsiders are refused. The call mutates state and is not idempotent: every invocation issues another set and discards the one before it, so a retry after a timeout returns codes different from those the first attempt generated. The codes come back unused, five of them of six characters with the default configuration, and a portal may be configured for a different number and length. Read the current set without changing it through `GET api/2.0/settings/tfaappcodes`. The authenticator secret itself is untouched, so the linked application keeps working.

## Parameters
This endpoint does not need any parameter.

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The newly generated backup codes, all unused, replacing the caller's previous set | [**TfaAppCodeArrayWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/tfa-app-code-array-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **405** | The authenticator method is not enabled on this portal, or the caller has no application linked | - | - |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**TfaAppCodeArrayWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/tfa-app-code-array-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#openid)

## HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
