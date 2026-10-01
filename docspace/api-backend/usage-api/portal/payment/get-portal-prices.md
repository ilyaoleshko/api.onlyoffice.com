# getPortalPrices

> getPortalPrices_200_response getPortalPrices()

`GET /api/2.0/portal/payment/prices`

Get the product prices

Lists what one unit of every purchasable product costs, keyed by the product name that `quantity` takes in the purchase operations, so a client can price a plan or a wallet service without reading the whole quota list. Nothing has to be called first, and the caller needs the permission to edit the portal settings, which portal administrators and the owner have. The call is read-only. Prices are given in the one currency resolved for this request from the portal region, which `GET api/2.0/portal/payment/currencies` reports; a product with no price in that currency comes back as `0` rather than being left out, so a zero means unpriced and not free. The list covers the products on offer, not the portal's own plan - the plan in force, with its limits and its usage, is `GET api/2.0/portal/payment/quota`.

## Parameters
This endpoint does not need any parameter.

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | Product name to the price of one unit in the currency of the request, `0` where the product has no price in it | [**getPortalPrices_200_response**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/get-portal-prices-200-response.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **403** | The caller may not edit the portal settings | - | - |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**getPortalPrices_200_response**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/get-portal-prices-200-response.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal.md#openid)

## HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
