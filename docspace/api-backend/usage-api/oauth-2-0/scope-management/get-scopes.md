# getScopes

> List getScopes()

`GET /api/2.0/oauth2/scopes`

List available OAuth2 scopes

Retrieves a list of all available OAuth2 scopes for the specified tenant. The scopes define the permissions that can be requested by OAuth2 clients. The list is ordered alphabetically, with the 'openid' scope always appearing first. It is a read-only catalogue that does not depend on which clients exist: a valid portal signature is the only requirement, with no role restriction, and every caller of the portal sees the same list.

## Parameters
This endpoint does not need any parameter.

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | Scopes successfully retrieved | [**List**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/scope-response.md) | - |
| **403** | Insufficient permissions to list scopes | [**ProblemDetail**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/problem-detail.md) | - |
| **406** | The Accept header does not allow application/json | [**ProblemDetail**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/problem-detail.md) | - |
| **429** | Too many requests - rate limit exceeded | [**ProblemDetail**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/problem-detail.md) | - |
| **500** | Internal server error occurred | [**ProblemDetail**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/problem-detail.md) | - |
| **405** | The HTTP method is not allowed for this path | [**ProblemDetail**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/problem-detail.md) | - |

## Return type

[**List**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/scope-response.md)

## Authorization

[x-signature](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/oauth-2-0.md#x-signature)

## HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
