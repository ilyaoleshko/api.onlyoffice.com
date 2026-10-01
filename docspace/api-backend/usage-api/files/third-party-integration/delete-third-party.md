# deleteThirdParty

> StringWrapper deleteThirdParty(providerId)

`DELETE /api/2.0/files/thirdparty/{providerId}`

Remove a third-party account

Disconnects a third-party storage account from the portal and returns the ID of the folder that stood for it, in the `provider-accountId` form the Files operations use for third-party entries. Take `providerId` from `GET api/2.0/files/thirdparty`: it is the numeric account ID, not that composed folder ID. The member who connected the account can remove it; another member's request is refused unless they hold delete rights on the folder it stands for. Nothing is deleted at the storage service: the files stay with the provider, and what goes away is the portal's link to them together with the stored credentials, the sharing records and the tags kept for its entries. A room that was created on this account stops being available. When the account being removed is the one connected for backups by `POST api/2.0/files/thirdparty/backup`, its backup schedule is deleted as well. The removal cannot be repeated: once the account is gone the same ID is refused rather than confirmed, so treat the first successful answer as the record of it.

## Parameters

|Name | In | Type | Description | Notes |
|------------- | ------------- | ------------- | ------------- | -------------|
| **providerId** | path | **Integer** (int32) | The ID of the connected third-party storage account, as `providerId` of `GET api/2.0/files/thirdparty`. | [required] [example: `12`] |

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The ID of the folder that stood for the removed account | [**StringWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/string-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **400** | Bad Request. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**StringWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/string-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#openid)

## HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
