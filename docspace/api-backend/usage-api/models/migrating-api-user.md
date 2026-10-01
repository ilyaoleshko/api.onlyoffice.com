# MigratingApiUser
The migrating user parameters.

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
| **shouldImport** | **Boolean** | Specifies whether the API entity should be imported. | [optional] |
| **key** | **String** | The user key. | [optional] [nullable] |
| **email** | **String** (email) | The user email. | [optional] [nullable] |
| **displayName** | **String** | The user display name. | [optional] [nullable] |
| **firstName** | **String** | The user first name. | [optional] [nullable] |
| **lastName** | **String** | The user last name. | [optional] [nullable] |
| **userType** | [**EmployeeType**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/employee-type.md) | The user type. | [optional] [enum: `All`, `RoomAdmin`, `Guest`, `DocSpaceAdmin`, `User`] |
| **migratingFiles** | [**MigratingApiFiles**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/migrating-api-files.md) | The user's migrating files. | [optional] |
