# DocsCloudConfig
Represents the configuration of a Docs Connect tenant.

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
| **tenantName** | **String** | The tenant name. | [optional] [example: `My Portal`] [minLength: 0] [maxLength: 255] [nullable] |
| **security** | [**DocsCloudSecurityConfig**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/docs-cloud-security-config.md) | The security configuration. | [optional] |
| **server** | [**DocsCloudServerConfig**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/docs-cloud-server-config.md) | The server configuration. | [optional] |
| **wopi** | [**DocsCloudWopiConfig**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/docs-cloud-wopi-config.md) | The WOPI configuration. | [optional] |
| **ipFilter** | [**DocsCloudIpFilterConfig**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/docs-cloud-ip-filter-config.md) | The IP filter configuration. | [optional] |
