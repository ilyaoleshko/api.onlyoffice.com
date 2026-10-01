# getPaymentUrl

> StringWrapper getPaymentUrl(PaymentUrlRequestDto)

`PUT /api/2.0/portal/payment/url`

Get the payment page URL

Starts the purchase of a monthly paid plan for this portal by handing back the hosted checkout page the buyer has to open; nothing is bought until that page is completed. The portal must have no paid plan yet - a portal whose plan is already paid gets an empty result and changes its subscription through `PUT api/2.0/portal/payment/update` instead - and the product name in `quantity` must be one of the monthly, non-wallet plans listed by `GET api/2.0/portal/payment/quotas`. Only a DocSpace administrator may call it. The call itself changes nothing on the portal and may be repeated: the money is taken by the payment provider on the checkout page, and the plan becomes active once the provider confirms it. The returned URL is absolute and single-purpose - it carries the caller's e-mail, the language of the request and the currency of the request region, and it redirects to `successUrl` or `backUrl` when the buyer finishes or cancels. Exactly one product per call is accepted and its quantity has to be greater than zero; yearly and wallet products are refused, and wallet services are bought with `PUT api/2.0/portal/payment/updatewallet` instead.

## Parameters

|Name | In | Type | Description | Notes |
|------------- | ------------- | ------------- | ------------- | -------------|
| **PaymentUrlRequestDto** | body | [**PaymentUrlRequestDto**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/payment-url-request-dto.md) |  | [optional] |

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The absolute URL of the checkout page to open, or an empty result when the portal already has a paid plan | [**StringWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/string-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **400** | `quantity` holds more than one product, a quantity that is not greater than zero, or a product that is not a monthly plan | - | - |
| **403** | The caller is not a DocSpace administrator, or the portal has no billing service configured | - | - |
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

- **Content-Type**: application/json
- **Accept**: application/json
