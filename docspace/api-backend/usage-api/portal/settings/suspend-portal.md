# suspendPortal

> suspendPortal()

`PUT /api/2.0/portal/suspend`

Deactivate a portal

Deactivates this portal: its status becomes suspended and its users can no longer work in it, while all of its rooms, files and accounts stay untouched. It is reached only with the deactivation link that `POST api/2.0/portal/suspend` mails to the portal owner - that link authorizes the call instead of an authentication token - and the owner is checked again here, so a link issued for another account is refused. On a server installation the last remaining space cannot be deactivated. The call is mutating and idempotent: it sets the status, records the deactivation in the audit trail and refreshes the portal's base domain, and repeating it leaves the portal suspended. Nothing is returned in the body; the new state is read from `status` in `GET api/2.0/portal`. Bring the portal back with `PUT api/2.0/portal/continue`, using the second link from the same letter. To remove the portal and its content for good, use `DELETE api/2.0/portal/delete` instead - that cannot be undone.

## Parameters
This endpoint does not need any parameter.

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The portal is now suspended, its users can no longer work in it and its content is kept; the response carries no content | - | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

null (empty response body)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#openid)

## HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
