# aiAgentsUpdateQuota request body

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
| **roomIds** | [**List**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-agents-update-quota-request-room-ids-item.md) | Agent (room) ids to update. | [required] |
| **quota** | **BigDecimal** | New quota in bytes; a negative value disables the custom quota. | [required] |
