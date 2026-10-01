# ONLYOFFICE DocSpace Migration API

The browsable version of this reference, with a request builder and code samples, is published at
[https://api.onlyoffice.com/docspace/api-backend/usage-api/](https://api.onlyoffice.com/docspace/api-backend/usage-api/).

All URIs are relative to *https://yourportal.onlyoffice.com*, where the host is the address of your DocSpace instance.

## Migration

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**cancelMigration**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/migration/cancel-migration.md) | **POST** /api/2.0/migration/cancel | Cancel migration |
| [**clearMigration**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/migration/clear-migration.md) | **POST** /api/2.0/migration/clear | Clear migration |
| [**finishMigration**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/migration/finish-migration.md) | **POST** /api/2.0/migration/finish | Finish migration |
| [**getMigrationLogs**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/migration/get-migration-logs.md) | **GET** /api/2.0/migration/logs | Get migration logs |
| [**getMigrationStatus**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/migration/get-migration-status.md) | **GET** /api/2.0/migration/status | Get migration status |
| [**listMigrations**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/migration/list-migrations.md) | **GET** /api/2.0/migration/list | Get available migrators |
| [**startMigration**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/migration/start-migration.md) | **POST** /api/2.0/migration/migrate | Start migration |
| [**uploadAndInitializeMigration**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/migration/upload-and-initialize-migration.md) | **POST** /api/2.0/migration/init/\{migratorName\} | Parse migration archive |

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

