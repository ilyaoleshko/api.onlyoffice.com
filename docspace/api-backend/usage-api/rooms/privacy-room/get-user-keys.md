# getUserKeys

> EncryptionKeyArrayWrapper getUserKeys()

`GET /api/2.0/privacyroom/keys`

Get own encryption keys

Returns every encryption key pair the calling user holds, the encrypted private half included, which is the material a client needs in order to decrypt content in a private room. The set is personal and there is no parameter for another user's keys: an authenticated caller reads only their own, and a guest, who cannot own key material at all, always reads an empty set. The call is read-only. An empty answer, whether an empty list or none at all, means no key has been created yet, and until `POST api/2.0/privacyroom/keys` creates one the user cannot be invited to a private room. Each entry carries the pair's `id`, its owner in `userId`, the moment the material was stored in `date`, the public half, the private half encrypted with the user's password, and the portal-wide crypto engine in `cryptoEngineId`. For the keys that open a whole private room use `GET api/2.0/privacyroom/{roomId}/access`, and for the keys a single file is shared with use `GET api/2.0/files/file/{fileId}/publickeys`; this operation is about the caller alone.

## Parameters
This endpoint does not need any parameter.

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The encryption keys of the current user | [**EncryptionKeyArrayWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/encryption-key-array-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**EncryptionKeyArrayWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/encryption-key-array-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#openid)

## HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
