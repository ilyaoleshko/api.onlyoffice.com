# cancelMigration

> cancelMigration()

`POST /api/2.0/migration/cancel`

Cancel migration

Stops the parse pass queued for this portal and deletes the backup uploaded for it - the way back from a wrong archive or a wrong migrator name. Nothing has to be called first and a DocSpace administrator is required; the request is only queued, so the parse ends shortly after the call returns and `GET api/2.0/migration/status` stops reporting it. The call is destructive for the uploaded data: the whole upload folder is removed and the backup has to be sent to `migrationFileUpload.ashx` again before a new parse. It is idempotent - cancelling when nothing is running still answers 200 - and it undoes nothing that was already written to the portal. Only the parse stage is stopped, the job whose `parseResult.operation` is `parse`: an import started by `POST api/2.0/migration/migrate` keeps running, and a finished import is discarded with `POST api/2.0/migration/clear` instead.

## Parameters
This endpoint does not need any parameter.

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The cancellation has been queued; the parse stops and the uploaded backup is deleted. The response carries no content | - | `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset` |
| **403** | The caller is not a DocSpace administrator | - | - |
| **401** | Unauthorized | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **429** | Too Many Requests. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | `Retry-After` |
| **500** | Internal Server Error. | [**ErrorApiResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/error-api-response.md) | - |
| **502** | Bad Gateway. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |
| **503** | Service Unavailable. Returned by the reverse proxy, response body may be HTML and not JSON. | - | - |

## Return type

null (empty response body)

## Authorization

[Basic](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/migration.md#basic), [OAuth2](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/migration.md#oauth2) (scopes: read, write), [ApiKeyBearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/migration.md#apikeybearer), [asc_auth_key](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/migration.md#asc_auth_key), [Bearer](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/migration.md#bearer), [OpenId](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/migration.md#openid)

## HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
