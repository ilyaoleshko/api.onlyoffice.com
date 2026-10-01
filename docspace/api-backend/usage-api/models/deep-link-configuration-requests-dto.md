# DeepLinkConfigurationRequestsDto
How the portal opens its links on a mobile device.

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
| **deepLinkSettings** | [**TenantDeepLinkSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/tenant-deep-link-settings.md) | The deep link configuration to store. Only its `handlingMode` is read - whether a link always opens in the browser, always in the native application, or asks the user each time - and a mode outside the defined set is refused with 400 before anything is stored. | [optional] |
