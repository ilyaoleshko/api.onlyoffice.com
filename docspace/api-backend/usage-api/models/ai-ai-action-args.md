# AiAiActionArgs

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
| **tools** | [**List**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-tmcp-item.md) | Extra tools offered to the model for this request. | [optional] [example: `[]`] |
| **isReasoning** | **Boolean** | Legacy extended-thinking switch; stands for `medium`. `reasoningLevel` wins when both are set. | [optional] [example: `false`] |
| **reasoningLevel** | [**AiAiReasoningLevel**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-ai-reasoning-level.md) | Depth of extended thinking for the round; providers clamp it to what the model accepts. | [optional] [enum: `off`, `low`, `medium`, `high`, `max`] |
| **prompt** | [**AiAiActionArgs_prompt**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-ai-action-args-prompt.md) |  | [optional] |
