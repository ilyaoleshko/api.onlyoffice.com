# changeUserEmail

> EmployeeFullWrapper changeUserEmail(userid, ChangeEmailRequest)

`PUT /api/2.0/people/{userid}/email`

Change a user email

Sets a new email address on an account, which is the step that completes an email change. The request has to carry the confirmation token from the emailed link rather than an ordinary session, and an expired or already used token is answered with 401. The account has to exist and be `Active`, and only the portal owner may change the owner's own address. Pass the address either in plain text as `email` or, as it arrives inside the confirmation link, encrypted as `encEmail`; an empty or malformed address answers 400. An address equal to the current one is accepted and changes nothing, while a new one is stored in lowercase and marks the account `Activated`, because following the link proves the address works. The answer is the profile with its new address. The change is requested through `POST api/2.0/people/email`, which is what sends the link.

## Parameters

|Name | In | Type | Description | Notes |
|------------- | ------------- | ------------- | ------------- | -------------|
| **userid** | path | **UUID** (uuid) | The ID of the account whose address is set, taken from the route. It has to match the account the confirmation token was issued for, and the account has to be active. | [required] [example: `00000000-0000-0000-0000-000000000000`] |
| **ChangeEmailRequest** | body | [**ChangeEmailRequest**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/change-email-request.md) | The new address, in plain text or in the encrypted form the confirmation link carries. | [required] |

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The profile with its new address | [**EmployeeFullWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/employee-full-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **400** | The user ID is empty, or the address is missing or malformed | - | - |
| **403** | The account is not active, or only its owner may change this address | - | - |
| **404** | No account has the specified ID | - | - |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**EmployeeFullWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/employee-full-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/people.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/people.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/people.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/people.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/people.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/people.md#openid)

## HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json
