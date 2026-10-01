# AiImportResult
Outcome of `PromptsEngine.importBundle`. Either every entry persisted with counts, or no entries persisted plus a per-entry error report.

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
| **success** | **Boolean** | True when the whole bundle was imported. | [required] [example: `true`] |
| **imported** | [**AiImportResult_imported**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-import-result-imported.md) |  | [optional] |
| **errors** | [**List**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/ai-import-error.md) | What was rejected, per entry. Present on failure - and then nothing was imported. | [optional] [example: `[]`] |
