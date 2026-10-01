# storeForcesave

> BooleanWrapper storeForcesave()

`PUT /api/2.0/files/storeforcesave`

Change the ability to store the forcesaved files

Reports that forcesaved versions are not kept as separate file versions in this portal. The operation is a stub kept for compatibility: it takes no request body, stores nothing and always answers false, so it neither turns the behaviour on nor off and repeating it changes nothing. What it describes is what happens to the intermediate saves the editor makes while a document is still open - they update the current version instead of piling up as new ones in `GET api/2.0/files/file/{fileId}/history`. Any authenticated role down to a guest may call it; an unauthenticated caller is refused. The same constant is published as `storeForcesave` by `GET api/2.0/files/settings`, which is the cheaper way to read it. Its companion stub `PUT api/2.0/files/forcesave` answers for forcesaving itself in the same way. Version history is not affected by this call either: the versions a document really has are the ones the file history operation lists, and a new one appears when the editing session is closed.

## Parameters
This endpoint does not need any parameter.

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | Always false: forcesaved versions are not kept separately | [**BooleanWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/boolean-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**BooleanWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/boolean-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#openid)

## HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
