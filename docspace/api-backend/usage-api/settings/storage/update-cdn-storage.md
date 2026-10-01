# updateCdnStorage

> CdnStorageSettingsWrapper updateCdnStorage(StorageRequestsDto)

`PUT /api/2.0/settings/storage/cdn`

Update the CDN storage

Selects the content delivery network that serves the static content of the portal and saves the credentials it needs: `module` is the identifier of one of the entries of `GET api/2.0/settings/storage/cdn`, and `props` carries that provider's authentication keys as name and value pairs. The provider has to be available on the server, which the `isSet` flag of the listing tells, otherwise the request is rejected as invalid. Sending the module the portal already uses changes nothing and returns the saved settings as they are. Any other module is saved and the upload of the static content is handed to the storage service; the settings come back only when that hand-over succeeds, a failure being reported as a server error. Unlike the portal storage this has no progress operation, so there is nothing to poll: the content appears on the CDN once the service has copied it. Only static content is affected here, never documents; for those use `PUT api/2.0/settings/storage`. The caller needs the permission to edit portal settings, which in practice means the portal owner or a DocSpace admin, on a server installation with an unrestricted access space. The response is the stored CDN configuration.

## Parameters

|Name | In | Type | Description | Notes |
|------------- | ------------- | ------------- | ------------- | -------------|
| **StorageRequestsDto** | body | [**StorageRequestsDto**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/storage-requests-dto.md) |  | [optional] |

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The saved CDN configuration; the upload of the static content has been handed to the storage service | [**CdnStorageSettingsWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/cdn-storage-settings-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **400** | The requested CDN module is not configured on this installation | - | - |
| **403** | The caller may not edit portal settings, or this installation does not allow changing the storage | - | - |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**CdnStorageSettingsWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/cdn-storage-settings-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings.md#openid)

## HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json
