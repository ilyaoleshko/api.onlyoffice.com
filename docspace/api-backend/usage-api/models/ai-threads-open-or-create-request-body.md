# aiThreadsOpenOrCreate request body

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
| **threadId** | **String** |  | [optional] |
| **profile** | [**AiProfile**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-profile.md) | Profile the title generation runs on. | [required] |
| **profileId** | **String** |  | [required] |
| **firstMessage** | [**AiThreadMessageLike**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-thread-message-like.md) | First user message a fresh thread derives its title from. | [required] |
| **entityId** | **String** | Opaque scope token persisted on a freshly created thread. | [optional] |
| **entityMeta** | [**aiThreadsOpenOrCreate_request_entityMeta**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-threads-open-or-create-request-entity-meta.md) |  | [optional] |
