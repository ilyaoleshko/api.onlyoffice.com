# getCommonThirdPartyFolders

> FolderStringArrayWrapper getCommonThirdPartyFolders()

`GET /api/2.0/files/thirdparty/common`

Get common third-party folders

Lists the third-party storage accounts attached to the legacy Common section, as folder entries that can be browsed with the usual folder operations. Each entry stands for a whole connected account: its title is the account title, and `providerId` and `providerKey` identify the account behind it. Only accounts whose owner the caller may read are included, so the answer differs from one member to another. The call is read-only and returns a plain array with no paging. An empty array is the expected answer in most portals and does not mean an error: accounts connected by `POST api/2.0/files/thirdparty` are attached to the Rooms section, not to Common, so only accounts inherited from an older portal appear here. The list is also empty while the portal-wide third-party switch is off (`PUT api/2.0/files/thirdparty`) and when no storage service is configured. For the accounts the caller owns, regardless of where they are attached, use `GET api/2.0/files/thirdparty`.

## Parameters
This endpoint does not need any parameter.

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The third-party accounts attached to the Common section, as folder entries | [**FolderStringArrayWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/folder-string-array-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**FolderStringArrayWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/folder-string-array-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#openid)

## HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
