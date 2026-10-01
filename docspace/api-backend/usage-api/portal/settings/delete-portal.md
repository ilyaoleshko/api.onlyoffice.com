# deletePortal

> StringWrapper deletePortal()

`DELETE /api/2.0/portal/delete`

Delete a portal

Removes this portal for good: its rooms, files, accounts, settings and OAuth clients go with it and its domain stops serving the portal. It is reached only with the removal link that `POST api/2.0/portal/delete` mails to the portal owner - that link authorizes the call instead of an authentication token - and the owner is checked again here; on a server installation the last remaining space cannot be removed. The call is destructive and cannot be undone, and there is no restore operation, so take a backup with `POST api/2.0/backup/startbackup` first when the content still matters. It keeps working while the portal's payment has lapsed. Along the way the portal is dropped from the hosting cache, the owner is mailed a confirmation, the removal is written to the audit trail and, for a portal that was paying, the support team is notified as well. The answer is the absolute URL of the feedback form to send the departing owner to. To pause the portal instead of erasing it, use `PUT api/2.0/portal/suspend`.

## Parameters
This endpoint does not need any parameter.

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The absolute URL of the feedback form to send the owner of the removed portal to | [**StringWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/string-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**StringWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/string-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#openid)

## HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
