# sendEditorNotify

> AceShortWrapperArrayWrapper sendEditorNotify(fileId, MentionMessageWrapper)

`POST /api/2.0/files/file/{fileId}/sendeditornotify`

Notify mentioned users

Emails the people named in `emails` that they were mentioned in a file, with a link that opens the file at the place the mention sits when `actionLink` carries the anchor the editor produced. Only addresses that belong to portal accounts are notified: an address that belongs to nobody is skipped, and the note is cut to its first 200 characters in the mail, while a `message` longer than the field allows is refused with 400. The answer is usually empty: the access list of the file comes back when the file is encrypted, or when one of the addresses belongs to nobody and the caller may share the file - that is then the cue to invite that person with `PUT api/2.0/files/file/{id}/share`. The caller needs comment rights, which the creator of the file, the manager of its room and a member invited to comment, review or edit have, while a guest or a member without access is refused with 403; a file that does not exist answers with 404 and a file in the trash is refused. The operation is rate-limited and answers 429 once the caller sends too many notifications. A delivery failure is swallowed, so 200 does not prove that the mail left the portal.

## Parameters

|Name | In | Type | Description | Notes |
|------------- | ------------- | ------------- | ------------- | -------------|
| **fileId** | path | **Integer** (int32) | The file the mention was made in. A file stored on the portal is numbered, while a file in a connected third-party account is named by an opaque string. | [required] [example: `10`] |
| **MentionMessageWrapper** | body | [**MentionMessageWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/mention-message-wrapper.md) | The notification to send. | [optional] |

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The people who currently have access to the file, when the caller still has to invite someone; empty otherwise | [**AceShortWrapperArrayWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ace-short-wrapper-array-wrapper.md) | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **400** | The address list is missing, or the message is longer than the field allows | - | - |
| **403** | The caller may not comment on the file | - | - |
| **404** | The file does not exist | - | - |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

[**AceShortWrapperArrayWrapper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ace-short-wrapper-array-wrapper.md)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files.md#openid)

## HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json
