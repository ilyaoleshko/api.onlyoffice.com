# startDocsCloudTrial

> BooleanWrapper startDocsCloudTrial()

`POST /api/2.0/settings/docscloud/trial`

Start the Docs Connect trial

Activates the free Docs Connect trial subscription for the current portal, and, once a Docs Connect server is assigned to the portal, allows the address of that server in the Content Security Policy settings. The portal tariff must be in the trial or paid state (not delayed and not unpaid), and the portal must not already hold a Docs Connect trial, Docs Connect or Docs Connect Dev Pack subscription: the quotas of the current tariff are listed by `GET api/2.0/portal/tariff`. The caller must be a portal administrator allowed to edit the portal settings, on an installation where the billing service is configured. The operation changes the portal subscription and is not idempotent: repeating it after a successful activation fails with 400. It returns `true` when the trial has been granted, and `false` when the billing service declines it (for example, when this portal has already used its trial), in which case nothing is changed. It never buys a paid plan: an existing paid Docs Connect subscription is moved to Docs Connect Dev Pack by `POST api/2.0/settings/docscloud/switchtodevpack` instead.

## Parameters
This endpoint does not need any parameter.

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | Boolean value: true if the trial subscription is activated, false if the billing service declines it | [**BooleanWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/boolean-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **400** | The portal already has a Docs Connect trial, Docs Connect or Docs Connect Dev Pack subscription | - | - |
| **402** | The portal tariff is delayed or not paid, so the trial cannot be started | - | - |
| **403** | The caller is not allowed to edit the portal settings, or the billing service is not configured | - | - |
| **404** | The Docs Connect trial quota is not available on this installation | - | - |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**BooleanWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/boolean-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#openid)

## HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
