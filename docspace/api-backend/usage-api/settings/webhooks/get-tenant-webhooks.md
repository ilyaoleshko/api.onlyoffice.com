# getTenantWebhooks

> WebhooksConfigWithStatusArrayWrapper getTenantWebhooks()

`GET /api/2.0/settings/webhook`

Get the portal webhooks

Returns the webhook subscriptions of the current portal, each together with the outcome of its most recent delivery. The portal owner and a `DocSpaceAdmin` see every subscription in the portal, while a `RoomAdmin` or a `User` sees only the ones they created themselves, so the same call answers differently depending on who asks. A `Guest` may not use webhooks at all and is refused, and so is any non-admin caller while the portal keeps the developer tools restricted, which `GET api/2.0/settings/devtoolsaccess` reports. Every entry pairs the stored configuration with `status`, the HTTP status code the target answered on the last attempt, where 0 means nothing has been delivered yet, while the secret key is not part of the response. The list is neither paginated nor ordered, and an empty list simply means no subscription exists for the caller. Nothing is written and the call is safe to repeat. Create a subscription with `POST api/2.0/settings/webhook`, and inspect single deliveries with `GET api/2.0/settings/webhooks/log`.

## Parameters
This endpoint does not need any parameter.

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The webhook subscriptions visible to the caller, each with the status of its last delivery | [**WebhooksConfigWithStatusArrayWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/webhooks-config-with-status-array-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **403** | The caller is a `Guest`, or a non-admin caller while the developer tools are restricted | - | - |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**WebhooksConfigWithStatusArrayWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/webhooks-config-with-status-array-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#openid)

## HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
