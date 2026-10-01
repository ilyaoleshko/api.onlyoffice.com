# ONLYOFFICE DocSpace Security API

The browsable version of this reference, with a request builder and code samples, is published at
[https://api.onlyoffice.com/docspace/api-backend/usage-api/](https://api.onlyoffice.com/docspace/api-backend/usage-api/).

All URIs are relative to *https://yourportal.onlyoffice.com*, where the host is the address of your DocSpace instance.

## Access to DevTools

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**setTenantDevToolsAccessSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/access-to-devtools/set-tenant-dev-tools-access-settings.md) | **POST** /api/2.0/settings/devtoolsaccess | Set the Developer Tools access settings |

## Active connections

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getAllActiveConnections**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/active-connections/get-all-active-connections.md) | **GET** /api/2.0/security/activeconnections | Get active connections |
| [**logOutActiveConnection**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/active-connections/log-out-active-connection.md) | **PUT** /api/2.0/security/activeconnections/logout/\{loginEventId\} | Log out one connection |
| [**logOutAllActiveConnectionsChangePassword**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/active-connections/log-out-all-active-connections-change-password.md) | **PUT** /api/2.0/security/activeconnections/logoutallchangepassword | Log out and reset password |
| [**logOutAllActiveConnectionsForUser**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/active-connections/log-out-all-active-connections-for-user.md) | **PUT** /api/2.0/security/activeconnections/logoutall/\{userId\} | Log out a user everywhere |
| [**logOutAllExceptThisConnection**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/active-connections/log-out-all-except-this-connection.md) | **PUT** /api/2.0/security/activeconnections/logoutallexceptthis | Log out other connections |

## Audit trail data

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**createAuditTrailReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/audit-trail-data/create-audit-trail-report.md) | **POST** /api/2.0/security/audit/events/report | Start audit trail report |
| [**getAuditEventsByFilter**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/audit-trail-data/get-audit-events-by-filter.md) | **GET** /api/2.0/security/audit/events/filter | Get filtered audit events |
| [**getAuditSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/audit-trail-data/get-audit-settings.md) | **GET** /api/2.0/security/audit/settings/lifetime | Get audit lifetime settings |
| [**getAuditTrailMappers**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/audit-trail-data/get-audit-trail-mappers.md) | **GET** /api/2.0/security/audit/mappers | Get audit trail mappers |
| [**getAuditTrailReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/audit-trail-data/get-audit-trail-report.md) | **GET** /api/2.0/security/audit/events/report | Get audit trail report status |
| [**getAuditTrailTypes**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/audit-trail-data/get-audit-trail-types.md) | **GET** /api/2.0/security/audit/types | Get audit trail types |
| [**getLastAuditEvents**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/audit-trail-data/get-last-audit-events.md) | **GET** /api/2.0/security/audit/events/last | Get recent audit events |
| [**setAuditSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/audit-trail-data/set-audit-settings.md) | **POST** /api/2.0/security/audit/settings/lifetime | Set audit lifetime settings |
| [**terminateAuditTrailReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/audit-trail-data/terminate-audit-trail-report.md) | **DELETE** /api/2.0/security/audit/events/report | Terminate audit trail report |

## Banners visibility

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**setTenantBannerSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/banners-visibility/set-tenant-banner-settings.md) | **POST** /api/2.0/settings/banner | Set the banners visibility |

## CSP

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**configureCsp**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/csp/configure-csp.md) | **POST** /api/2.0/security/csp | Configure CSP settings |
| [**getCspSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/csp/get-csp-settings.md) | **GET** /api/2.0/security/csp | Get CSP settings |

## Firebase

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**docRegisterPusnNotificationDevice**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/firebase/doc-register-pusn-notification-device.md) | **POST** /api/2.0/settings/push/docregisterdevice | Register a push device |
| [**subscribeDocumentsPushNotification**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/firebase/subscribe-documents-push-notification.md) | **PUT** /api/2.0/settings/push/docsubscribe | Set push subscription |

## Login history

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**createLoginHistoryReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/login-history/create-login-history-report.md) | **POST** /api/2.0/security/audit/login/report | Start login history report |
| [**getLastLoginEvents**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/login-history/get-last-login-events.md) | **GET** /api/2.0/security/audit/login/last | Get recent login events |
| [**getLoginEventsByFilter**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/login-history/get-login-events-by-filter.md) | **GET** /api/2.0/security/audit/login/filter | Get filtered login events |
| [**getLoginHistoryReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/login-history/get-login-history-report.md) | **GET** /api/2.0/security/audit/login/report | Get login history report status |
| [**terminateLoginHistoryReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/login-history/terminate-login-history-report.md) | **DELETE** /api/2.0/security/audit/login/report | Terminate login history report |

## OAuth2

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**generateJwtToken**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/oauth2/generate-jwt-token.md) | **GET** /api/2.0/security/oauth2/token | Generate JWT token |

## SMTP settings

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getSmtpOperationStatus**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/smtp-settings/get-smtp-operation-status.md) | **GET** /api/2.0/smtpsettings/smtp/test/status | Get SMTP test status |
| [**getSmtpSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/smtp-settings/get-smtp-settings.md) | **GET** /api/2.0/smtpsettings/smtp | Get SMTP settings |
| [**resetSmtpSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/smtp-settings/reset-smtp-settings.md) | **DELETE** /api/2.0/smtpsettings/smtp | Reset SMTP settings |
| [**saveSmtpSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/smtp-settings/save-smtp-settings.md) | **POST** /api/2.0/smtpsettings/smtp | Save SMTP settings |
| [**testSmtpSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/security/smtp-settings/test-smtp-settings.md) | **GET** /api/2.0/smtpsettings/smtp/test | Test SMTP settings |

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

