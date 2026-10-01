# aiAiSendCustom request body

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
| **isStream** | **Boolean** | Stream the reply (ndjson) when true, else return a single message. | [required] |
| **systemPrompt** | **String** | Caller-supplied system prompt for this one-turn call. | [required] |
| **userMessage** | [**AiThreadMessageLike**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-thread-message-like.md) |  | [required] |
| **actionArgs** | [**AiAiActionArgs**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-ai-action-args.md) | Per-request engine options: extra tools, reasoning, prompt override. | [optional] |
