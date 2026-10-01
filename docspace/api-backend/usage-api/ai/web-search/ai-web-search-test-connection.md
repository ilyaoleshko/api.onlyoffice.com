# aiWebSearchTestConnection

> aiProfilesTestConnection_200_response aiWebSearchTestConnection(AiWebSearchConfig)

`POST /api/2.0/ai/web-search/test-connection`

Test a web-search provider

Probes a web-search configuration against the live provider and reports the outcome, storing nothing - this is what a Test button calls so that a failure commits no state. The configuration is taken from the request rather than from storage, so credentials that were never saved can be checked. A `baseUrl` pointing at a private network address is refused before any request leaves the portal. The verdict is carried in the body rather than in the status, so a failed probe still answers 200 and the caller has to read the payload.

## Parameters

|Name | In | Type | Description | Notes |
|------------- | ------------- | ------------- | ------------- | -------------|
| **AiWebSearchConfig** | body | [**AiWebSearchConfig**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-web-search-config.md) |  | [required] |

## Responses

| Status code | Description | Type | Response headers |
|------------- | ------------- | ------------- | -------------|
| **200** | The outcome of the probe. A failed probe is reported here, not as a status. | [**aiProfilesTestConnection_200_response**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-profiles-test-connection-200-response.md) | - |
| **400** | The configuration is missing or malformed, or the provider URL points at a private network address. | [**AiErrorResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-error-response.md) | - |
| **401** | Missing `asc_auth_key` cookie or `Authorization` header. | [**AiErrorResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-error-response.md) | - |
| **403** | AI is disabled for this portal, or the caller is a guest. Relayed from the DocSpace AI service. | [**AiErrorResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-error-response.md) | - |
| **413** | The request body is larger than 100 KB, the JSON parser's limit on this route. | [**AiErrorResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-error-response.md) | - |
| **500** | Unhandled failure. The reason is logged server-side and never echoed back. | [**AiErrorResponse**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-error-response.md) | - |

## Return type

[**aiProfilesTestConnection_200_response**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-profiles-test-connection-200-response.md)

## Authorization

[cookieAuth](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai.md#cookieauth), [bearerAuth](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai.md#bearerauth)

## HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json
