# docRegisterPusnNotificationDevice

> FireBaseUserWrapper docRegisterPusnNotificationDevice(FirebaseRequestsDto)

`POST /api/2.0/settings/push/docregisterdevice`

Register a push device

Registers one mobile device of the calling user for the push notifications of the Documents application, by storing the Firebase token that device was issued together with the initial `isSubscribed` state. The token is handed out by Firebase to the mobile client, so obtain it there before calling: nothing here checks it, and it is kept as an opaque string of up to 255 characters. Every signed-in member registers its own devices, whatever its role - owner, administrator, user or guest - and a registration is bound to the caller and the current portal, so another member's devices cannot be touched. The call is safe to repeat, but it is not an update: a token already registered comes back as it stands and `isSubscribed` from the request is ignored, so switch an existing registration on or off with `PUT api/2.0/settings/push/docsubscribe` instead. What comes back is the stored registration, with `application` always `doc` and `isSubscribed` as stored. Only a subscribed device is sent the room activity messages, such as an invitation to a room, a role change, an archived room or a new document in a room, and only while the installation itself is configured with Firebase credentials.

## Parameters

|Name | In | Type | Description | Notes |
|------------- | ------------- | ------------- | ------------- | -------------|
| **FirebaseRequestsDto** | body | [**FirebaseRequestsDto**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/firebase-requests-dto.md) |  | [optional] |

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The stored device registration of the calling user, with the Firebase token, the `doc` application and the subscription state as they are kept | [**FireBaseUserWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/fire-base-user-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **400** | Bad Request. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**FireBaseUserWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/fire-base-user-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security.md#openid)

## HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json
