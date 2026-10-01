# ONLYOFFICE DocSpace AI API

The browsable version of this reference, with a request builder and code samples, is published at
[https://api.onlyoffice.com/docspace/api-backend/usage-api/](https://api.onlyoffice.com/docspace/api-backend/usage-api/).

All URIs are relative to *https://yourportal.onlyoffice.com*, where the host is the address of your DocSpace instance.

## AI

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**aiAiApproveToolCall**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/ai/ai-ai-approve-tool-call.md) | **POST** /api/2.0/ai/ai/approve-tool-call | Approve tool call |
| [**aiAiDenyToolCall**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/ai/ai-ai-deny-tool-call.md) | **POST** /api/2.0/ai/ai/deny-tool-call | Deny tool call |
| [**aiAiRegenerateStream**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/ai/ai-ai-regenerate-stream.md) | **POST** /api/2.0/ai/ai/regenerate-stream | Regenerate stream |
| [**aiAiSend**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/ai/ai-ai-send.md) | **POST** /api/2.0/ai/ai/send | Run an AI action |
| [**aiAiSendCustom**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/ai/ai-ai-send-custom.md) | **POST** /api/2.0/ai/ai/send-custom | Send custom |
| [**aiAiSendWithStream**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/ai/ai-ai-send-with-stream.md) | **POST** /api/2.0/ai/ai/send-with-stream | Send with stream |
| [**aiAiSendWithStreamOpenAI**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/ai/ai-ai-send-with-stream-open-ai.md) | **POST** /api/2.0/ai/ai/send-with-stream-openai | Stream a chat in OpenAI format |

## Agents

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**aiAgentsCreate**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/agents/ai-agents-create.md) | **POST** /api/2.0/ai/agents | Create an agent |
| [**aiAgentsDelete**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/agents/ai-agents-delete.md) | **DELETE** /api/2.0/ai/agents/\{id\} | Delete an agent |
| [**aiAgentsGet**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/agents/ai-agents-get.md) | **GET** /api/2.0/ai/agents/\{id\} | Get an agent |
| [**aiAgentsList**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/agents/ai-agents-list.md) | **GET** /api/2.0/ai/agents | List agents |
| [**aiAgentsNews**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/agents/ai-agents-news.md) | **GET** /api/2.0/ai/agents/news | List agent news items |
| [**aiAgentsResetQuota**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/agents/ai-agents-reset-quota.md) | **PUT** /api/2.0/ai/agents/resetquota | Reset agents' quota |
| [**aiAgentsUpdate**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/agents/ai-agents-update.md) | **PUT** /api/2.0/ai/agents/\{id\} | Update an agent |
| [**aiAgentsUpdateQuota**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/agents/ai-agents-update-quota.md) | **PUT** /api/2.0/ai/agents/agentquota | Update agents' quota |

## Assignments

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**aiAssignmentsAssign**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/assignments/ai-assignments-assign.md) | **PUT** /api/2.0/ai/assignments/assign | Bind a profile to an action |
| [**aiAssignmentsBulkAssign**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/assignments/ai-assignments-bulk-assign.md) | **PUT** /api/2.0/ai/assignments/bulk-assign | Bulk assign |
| [**aiAssignmentsCascadeProfileDelete**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/assignments/ai-assignments-cascade-profile-delete.md) | **DELETE** /api/2.0/ai/assignments/cascade-profile-delete | Cascade profile delete |
| [**aiAssignmentsGetAllAssignments**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/assignments/ai-assignments-get-all-assignments.md) | **GET** /api/2.0/ai/assignments/get-all-assignments | Get all assignments |
| [**aiAssignmentsGetAssignment**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/assignments/ai-assignments-get-assignment.md) | **GET** /api/2.0/ai/assignments/get-assignment | Get assignment |
| [**aiAssignmentsResolveForAction**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/assignments/ai-assignments-resolve-for-action.md) | **GET** /api/2.0/ai/assignments/resolve-for-action | Resolve for action |
| [**aiAssignmentsTryResolveForAction**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/assignments/ai-assignments-try-resolve-for-action.md) | **GET** /api/2.0/ai/assignments/try-resolve-for-action | Try resolve for action |
| [**aiAssignmentsUnassign**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/assignments/ai-assignments-unassign.md) | **DELETE** /api/2.0/ai/assignments/unassign | Clear an action's profile |

## Attachments

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**aiAttachmentsDelete**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/attachments/ai-attachments-delete.md) | **DELETE** /api/2.0/ai/attachments/delete | Delete one attachment |
| [**aiAttachmentsDeleteMany**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/attachments/ai-attachments-delete-many.md) | **DELETE** /api/2.0/ai/attachments/delete-many | Delete many |
| [**aiAttachmentsGet**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/attachments/ai-attachments-get.md) | **POST** /api/2.0/ai/attachments/get | Get one attachment |
| [**aiAttachmentsGetMany**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/attachments/ai-attachments-get-many.md) | **POST** /api/2.0/ai/attachments/get-many | Get many |
| [**aiAttachmentsLinkToMessage**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/attachments/ai-attachments-link-to-message.md) | **POST** /api/2.0/ai/attachments/link-to-message | Link to message |
| [**aiAttachmentsSaveFile**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/attachments/ai-attachments-save-file.md) | **POST** /api/2.0/ai/attachments/save-file | Save file |
| [**aiAttachmentsSaveFilesMany**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/attachments/ai-attachments-save-files-many.md) | **POST** /api/2.0/ai/attachments/save-files-many | Save files many |

## Editor tools

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**aiEditorToolsCall**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/editor-tools/ai-editor-tools-call.md) | **POST** /api/2.0/ai/editor-tools/call | Call an editor tool |
| [**aiEditorToolsList**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/editor-tools/ai-editor-tools-list.md) | **GET** /api/2.0/ai/editor-tools/list | List editor tools |

## Export

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**aiExportTextToDocx**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/export/ai-export-text-to-docx.md) | **POST** /api/2.0/ai/text-to-docx | Start markdown export |

## OpenAI passthrough

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**aiOpenaiChatCompletions**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/openai-passthrough/ai-openai-chat-completions.md) | **POST** /api/2.0/ai/openai/\{profileId\}/v1/chat/completions | OpenAI chat completions passthrough |
| [**aiOpenaiImagesGenerations**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/openai-passthrough/ai-openai-images-generations.md) | **POST** /api/2.0/ai/openai/\{profileId\}/v1/images/generations | OpenAI image generation passthrough |

## Preferences

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**aiPreferencesClearDeepMode**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/preferences/ai-preferences-clear-deep-mode.md) | **DELETE** /api/2.0/ai/preferences/clear-deep-mode | Clear deep mode |
| [**aiPreferencesGetDeepMode**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/preferences/ai-preferences-get-deep-mode.md) | **GET** /api/2.0/ai/preferences/get-deep-mode | Get deep mode |
| [**aiPreferencesGetReasoningLevel**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/preferences/ai-preferences-get-reasoning-level.md) | **GET** /api/2.0/ai/preferences/get-reasoning-level | Get reasoning level |
| [**aiPreferencesIsDeepModeSet**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/preferences/ai-preferences-is-deep-mode-set.md) | **GET** /api/2.0/ai/preferences/is-deep-mode-set | Is deep mode set |
| [**aiPreferencesSetDeepMode**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/preferences/ai-preferences-set-deep-mode.md) | **PUT** /api/2.0/ai/preferences/set-deep-mode | Set deep mode |
| [**aiPreferencesSetReasoningLevel**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/preferences/ai-preferences-set-reasoning-level.md) | **PUT** /api/2.0/ai/preferences/set-reasoning-level | Set reasoning level |

## Profiles

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**aiProfilesCreate**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/profiles/ai-profiles-create.md) | **POST** /api/2.0/ai/profiles/create | Create a provider profile |
| [**aiProfilesDelete**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/profiles/ai-profiles-delete.md) | **DELETE** /api/2.0/ai/profiles/delete | Delete a provider profile |
| [**aiProfilesGetById**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/profiles/ai-profiles-get-by-id.md) | **GET** /api/2.0/ai/profiles/get-by-id | Get a provider profile |
| [**aiProfilesList**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/profiles/ai-profiles-list.md) | **GET** /api/2.0/ai/profiles/list | List provider profiles |
| [**aiProfilesListModels**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/profiles/ai-profiles-list-models.md) | **GET** /api/2.0/ai/profiles/list-models | List models |
| [**aiProfilesListProviderModels**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/profiles/ai-profiles-list-provider-models.md) | **POST** /api/2.0/ai/profiles/list-provider-models | List provider models |
| [**aiProfilesTestConnection**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/profiles/ai-profiles-test-connection.md) | **POST** /api/2.0/ai/profiles/test-connection | Test a profile's provider |
| [**aiProfilesUpdate**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/profiles/ai-profiles-update.md) | **PUT** /api/2.0/ai/profiles/update | Update a provider profile |

## Prompts

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**aiPromptsCreate**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/prompts/ai-prompts-create.md) | **POST** /api/2.0/ai/prompts/create | Save a prompt |
| [**aiPromptsCreateFolder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/prompts/ai-prompts-create-folder.md) | **POST** /api/2.0/ai/prompts/create-folder | Create folder |
| [**aiPromptsDelete**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/prompts/ai-prompts-delete.md) | **DELETE** /api/2.0/ai/prompts/delete | Delete a saved prompt |
| [**aiPromptsDeleteFolder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/prompts/ai-prompts-delete-folder.md) | **DELETE** /api/2.0/ai/prompts/delete-folder | Delete folder |
| [**aiPromptsExport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/prompts/ai-prompts-export.md) | **GET** /api/2.0/ai/prompts/export | Export the prompt library |
| [**aiPromptsGetById**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/prompts/ai-prompts-get-by-id.md) | **GET** /api/2.0/ai/prompts/get-by-id | Get a saved prompt |
| [**aiPromptsGetFolderById**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/prompts/ai-prompts-get-folder-by-id.md) | **GET** /api/2.0/ai/prompts/get-folder-by-id | Get a prompt folder |
| [**aiPromptsImportBundle**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/prompts/ai-prompts-import-bundle.md) | **POST** /api/2.0/ai/prompts/import-bundle | Import bundle |
| [**aiPromptsList**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/prompts/ai-prompts-list.md) | **GET** /api/2.0/ai/prompts/list | List saved prompts |
| [**aiPromptsListFolders**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/prompts/ai-prompts-list-folders.md) | **GET** /api/2.0/ai/prompts/list-folders | List folders |
| [**aiPromptsMove**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/prompts/ai-prompts-move.md) | **PUT** /api/2.0/ai/prompts/move | Move a prompt to a folder |
| [**aiPromptsRenameFolder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/prompts/ai-prompts-rename-folder.md) | **PUT** /api/2.0/ai/prompts/rename-folder | Rename folder |
| [**aiPromptsUpdate**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/prompts/ai-prompts-update.md) | **PUT** /api/2.0/ai/prompts/update | Update a saved prompt |

## Settings

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**aiSettingsGet**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/settings/ai-settings-get.md) | **GET** /api/2.0/ai/config | Get AI settings |
| [**aiSettingsGetUser**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/settings/ai-settings-get-user.md) | **GET** /api/2.0/ai/config/user | Get user AI settings |
| [**aiSettingsGetVectorization**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/settings/ai-settings-get-vectorization.md) | **GET** /api/2.0/ai/config/vectorization | Get vectorization settings |
| [**aiSettingsSetUser**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/settings/ai-settings-set-user.md) | **PUT** /api/2.0/ai/config/user | Update user AI settings |
| [**aiSettingsSetVectorization**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/settings/ai-settings-set-vectorization.md) | **PUT** /api/2.0/ai/config/vectorization | Update vectorization settings |

## Threads

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**aiThreadsAppendUserMessage**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/threads/ai-threads-append-user-message.md) | **POST** /api/2.0/ai/threads/append-user-message | Append user message |
| [**aiThreadsClearMessages**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/threads/ai-threads-clear-messages.md) | **DELETE** /api/2.0/ai/threads/clear-messages | Clear messages |
| [**aiThreadsCreate**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/threads/ai-threads-create.md) | **POST** /api/2.0/ai/threads/create | Create a chat thread |
| [**aiThreadsDelete**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/threads/ai-threads-delete.md) | **DELETE** /api/2.0/ai/threads/delete | Delete a chat thread |
| [**aiThreadsDeleteMessage**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/threads/ai-threads-delete-message.md) | **DELETE** /api/2.0/ai/threads/delete-message | Delete message |
| [**aiThreadsGetById**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/threads/ai-threads-get-by-id.md) | **GET** /api/2.0/ai/threads/get-by-id | Get a chat thread |
| [**aiThreadsGetMessageById**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/threads/ai-threads-get-message-by-id.md) | **GET** /api/2.0/ai/threads/get-message-by-id | Get one chat message |
| [**aiThreadsList**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/threads/ai-threads-list.md) | **GET** /api/2.0/ai/threads/list | List chat threads |
| [**aiThreadsOpenOrCreate**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/threads/ai-threads-open-or-create.md) | **POST** /api/2.0/ai/threads/open-or-create | Open or create |
| [**aiThreadsReadMessages**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/threads/ai-threads-read-messages.md) | **GET** /api/2.0/ai/threads/read-messages | Read messages |
| [**aiThreadsRegenerateTitle**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/threads/ai-threads-regenerate-title.md) | **POST** /api/2.0/ai/threads/regenerate-title | Regenerate title |
| [**aiThreadsRename**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/threads/ai-threads-rename.md) | **PUT** /api/2.0/ai/threads/rename | Rename a chat thread |
| [**aiThreadsTouch**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/threads/ai-threads-touch.md) | **POST** /api/2.0/ai/threads/touch | Bump a thread's activity |
| [**aiThreadsUpdateMessage**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/threads/ai-threads-update-message.md) | **PUT** /api/2.0/ai/threads/update-message | Update message |

## Tools

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**aiToolsAddCustomServer**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/tools/ai-tools-add-custom-server.md) | **POST** /api/2.0/ai/tools/add-custom-server | Add custom server |
| [**aiToolsGetAllowAlways**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/tools/ai-tools-get-allow-always.md) | **GET** /api/2.0/ai/tools/get-allow-always | Get allow always |
| [**aiToolsGetCustomServer**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/tools/ai-tools-get-custom-server.md) | **GET** /api/2.0/ai/tools/get-custom-server | Get custom server |
| [**aiToolsGetDisabled**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/tools/ai-tools-get-disabled.md) | **GET** /api/2.0/ai/tools/get-disabled | Get disabled |
| [**aiToolsIsAllowAlways**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/tools/ai-tools-is-allow-always.md) | **GET** /api/2.0/ai/tools/is-allow-always | Is allow always |
| [**aiToolsIsToolDisabled**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/tools/ai-tools-is-tool-disabled.md) | **GET** /api/2.0/ai/tools/is-tool-disabled | Is tool disabled |
| [**aiToolsListCustomServers**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/tools/ai-tools-list-custom-servers.md) | **GET** /api/2.0/ai/tools/list-custom-servers | List custom servers |
| [**aiToolsListSystemTools**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/tools/ai-tools-list-system-tools.md) | **GET** /api/2.0/ai/tools/list-system-tools | List system tools |
| [**aiToolsRemoveCustomServer**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/tools/ai-tools-remove-custom-server.md) | **DELETE** /api/2.0/ai/tools/remove-custom-server | Remove custom server |
| [**aiToolsReplaceAllCustomServers**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/tools/ai-tools-replace-all-custom-servers.md) | **PUT** /api/2.0/ai/tools/replace-all-custom-servers | Replace all custom servers |
| [**aiToolsSetAllowAlways**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/tools/ai-tools-set-allow-always.md) | **PUT** /api/2.0/ai/tools/set-allow-always | Set allow always |
| [**aiToolsSetDisabled**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/tools/ai-tools-set-disabled.md) | **PUT** /api/2.0/ai/tools/set-disabled | Set disabled |
| [**aiToolsUpdateCustomServer**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/tools/ai-tools-update-custom-server.md) | **PUT** /api/2.0/ai/tools/update-custom-server | Update custom server |

## Vectorization

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**aiVectorizationStartTask**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/vectorization/ai-vectorization-start-task.md) | **POST** /api/2.0/ai/vectorization/tasks | Start a vectorization task |

## Web search

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**aiWebSearchClear**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/web-search/ai-web-search-clear.md) | **DELETE** /api/2.0/ai/web-search/clear | Clear the web-search configuration |
| [**aiWebSearchConfigure**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/web-search/ai-web-search-configure.md) | **PUT** /api/2.0/ai/web-search/configure | Configure and verify web search |
| [**aiWebSearchGetActiveConfig**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/web-search/ai-web-search-get-active-config.md) | **GET** /api/2.0/ai/web-search/get-active-config | Get active config |
| [**aiWebSearchIsConfigured**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/web-search/ai-web-search-is-configured.md) | **GET** /api/2.0/ai/web-search/is-configured | Is configured |
| [**aiWebSearchPassthroughContents**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/web-search/ai-web-search-passthrough-contents.md) | **POST** /api/2.0/ai/websearch/v1/contents | Web page contents passthrough |
| [**aiWebSearchPassthroughSearch**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/web-search/ai-web-search-passthrough-search.md) | **POST** /api/2.0/ai/websearch/v1/search | Web search passthrough |
| [**aiWebSearchSetActiveConfig**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/web-search/ai-web-search-set-active-config.md) | **PUT** /api/2.0/ai/web-search/set-active-config | Set active config |
| [**aiWebSearchTestConnection**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/ai/web-search/ai-web-search-test-connection.md) | **POST** /api/2.0/ai/web-search/test-connection | Test a web-search provider |

## Authorization

### cookieAuth
- **Type**: API key
- **API key parameter name**: asc_auth_key
- **Location**: 

### bearerAuth

- **Type**: HTTP Bearer Token authentication

### asc_auth_key
- **Type**: API key
- **API key parameter name**: asc_auth_key
- **Location**: 

### Basic

- **Type**: HTTP basic authentication

### Bearer

- **Type**: HTTP Bearer Token authentication (JWT)

### ApiKeyBearer
- **Type**: API key
- **API key parameter name**: ApiKeyBearer
- **Location**: HTTP header

### OAuth2

- **Type**: OAuth
- **Flow**: accessCode
- **Authorization URL**: 
- **Scopes**: 
  - read: Read access to protected resources
  - write: Write access to protected resources

### OpenId

### x-signature
- **Type**: API key
- **API key parameter name**: x-signature
- **Location**: 

