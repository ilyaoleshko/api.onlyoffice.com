# UserExistsResponseDto
The user existence check response parameters.

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
| **exists** | **Boolean** | Specifies whether the user exists or not. | [required] [example: `true`] |
| **status** | [**EmployeeStatus**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/employee-status.md) | The user status, if the user exists. | [optional] [enum: `1`, `2`, `4`, `5`, `7`] |
