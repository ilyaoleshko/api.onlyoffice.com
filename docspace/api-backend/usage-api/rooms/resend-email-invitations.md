# resendEmailInvitations

> resendEmailInvitations(id, UserInvitation)

`POST /api/2.0/files/rooms/{id}/resend`

Resend the room invitations

Sends the room invitation email again to members who were invited but have not joined yet. `resendAll` covers every pending invitation of the room and makes `usersIds` irrelevant, while an explicit list without that flag is limited to the named accounts. An account that has already accepted the invitation, is not a member of the room, or is invisible to the caller is skipped without an error, and a request that names nobody and does not set the flag does nothing, so a successful answer never proves that a message went out. Nothing about the room or its membership changes, and the operation can be repeated. The caller must be a manager of the room, an archived room is refused, a room template is answered as missing, and a malformed account id is rejected as an invalid request. The call is rate limited, so a client that loops over members should send one batch instead. The response carries no body.

## Parameters

|Name | In | Type | Description | Notes |
|------------- | ------------- | ------------- | ------------- | -------------|
| **id** | path | **Integer** (int32) | The room whose invitations are resent, named by the identifier that `GET api/2.0/files/rooms` reports for it. | [required] [example: `1`] |
| **UserInvitation** | body | [**UserInvitation**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/user-invitation.md) | Which pending invitations to send again. | [required] |

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The invitations that were still pending have been sent again | - | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **400** | Bad Request. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

null (empty response body)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/rooms.md#openid)

## HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json
