# ManageFormFillingDtoInteger
The action to apply to the filling of a PDF form.

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
| **formId** | **Integer** (int32) | The PDF form the action applies to. This is the value the operation reads, rather than the identifier in its route, and the two are to be sent the same. | [required] [example: `1`] |
| **action** | [**FormFillingManageAction**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/models/form-filling-manage-action.md) | The action to apply. | [optional] [enum: `0`, `1`, `2`, `3`] |
