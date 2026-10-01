# ONLYOFFICE DocSpace Settings API

The browsable version of this reference, with a request builder and code samples, is published at
[https://api.onlyoffice.com/docspace/api-backend/usage-api/](https://api.onlyoffice.com/docspace/api-backend/usage-api/).

All URIs are relative to *https://yourportal.onlyoffice.com*, where the host is the address of your DocSpace instance.

## Access to DevTools

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getTenantAccessDevToolsSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/access-to-devtools/get-tenant-access-dev-tools-settings.md) | **GET** /api/2.0/settings/devtoolsaccess | Get the Developer Tools access settings |

## Authorization

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getAuthServices**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/authorization/get-auth-services.md) | **GET** /api/2.0/settings/authservice | Get the authorization services |
| [**saveAuthKeys**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/authorization/save-auth-keys.md) | **POST** /api/2.0/settings/authservice | Save the authorization keys |
| [**testExternalDatabaseConnection**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/authorization/test-external-database-connection.md) | **POST** /api/2.0/settings/authservice/externaldb/test | Test external database connection |

## Banners visibility

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getTenantBannerSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/banners-visibility/get-tenant-banner-settings.md) | **GET** /api/2.0/settings/banner | Get the banners visibility |

## Common settings

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**closeAdminHelper**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/close-admin-helper.md) | **PUT** /api/2.0/settings/closeadminhelper | Close the admin helper |
| [**completeWizard**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/complete-wizard.md) | **PUT** /api/2.0/settings/wizard/complete | Complete the Wizard settings |
| [**configureDeepLink**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/configure-deep-link.md) | **POST** /api/2.0/settings/deeplink | Configure the deep link settings |
| [**deletePortalColorTheme**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/delete-portal-color-theme.md) | **DELETE** /api/2.0/settings/colortheme | Delete a color theme |
| [**getDeepLinkSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/get-deep-link-settings.md) | **GET** /api/2.0/settings/deeplink | Get the deep link settings |
| [**getPaymentSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/get-payment-settings.md) | **GET** /api/2.0/settings/payment | Get the payment settings |
| [**getPortalColorTheme**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/get-portal-color-theme.md) | **GET** /api/2.0/settings/colortheme | Get a color theme |
| [**getPortalHostname**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/get-portal-hostname.md) | **GET** /api/2.0/settings/machine | Get the portal hostname |
| [**getPortalLogo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/get-portal-logo.md) | **GET** /api/2.0/settings/logo | Get a portal logo |
| [**getPortalSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/get-portal-settings.md) | **GET** /api/2.0/settings | Get the portal settings |
| [**getSocketSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/get-socket-settings.md) | **GET** /api/2.0/settings/socket | Get the socket settings |
| [**getSupportedCultures**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/get-supported-cultures.md) | **GET** /api/2.0/settings/cultures | Get supported languages |
| [**getTenantAiAccessSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/get-tenant-ai-access-settings.md) | **GET** /api/2.0/settings/ai-access | Get the AI access settings |
| [**getTenantUserInvitationSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/get-tenant-user-invitation-settings.md) | **GET** /api/2.0/settings/invitationsettings | Get the user invitation settings |
| [**getTimeZones**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/get-time-zones.md) | **GET** /api/2.0/settings/timezones | Get time zones |
| [**saveDefaultFolder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/save-default-folder.md) | **PUT** /api/2.0/settings/defaultfolder | Set the default folder |
| [**saveDnsSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/save-dns-settings.md) | **PUT** /api/2.0/settings/dns | Save the DNS settings |
| [**saveMailDomainSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/save-mail-domain-settings.md) | **POST** /api/2.0/settings/maildomainsettings | Save the mail domain settings |
| [**savePortalColorTheme**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/save-portal-color-theme.md) | **PUT** /api/2.0/settings/colortheme | Save a color theme |
| [**setTenantAiAccessSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/set-tenant-ai-access-settings.md) | **POST** /api/2.0/settings/ai-access | Set the AI access settings |
| [**updateEmailActivationSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/update-email-activation-settings.md) | **PUT** /api/2.0/settings/emailactivation | Update the email activation settings |
| [**updateInvitationSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/common-settings/update-invitation-settings.md) | **PUT** /api/2.0/settings/invitationsettings | Update the user invitation settings |

## Cookies

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getCookieSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/cookies/get-cookie-settings.md) | **GET** /api/2.0/settings/cookiesettings | Get the cookie lifetime settings |
| [**updateCookieSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/cookies/update-cookie-settings.md) | **PUT** /api/2.0/settings/cookiesettings | Update the cookie lifetime settings |

## DocsCloud

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**calculateDevPack**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/docscloud/calculate-dev-pack.md) | **POST** /api/2.0/settings/docscloud/calculatedevpack | Calculate the Docs Connect Dev Pack switch cost |
| [**createTenantQuotaReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/docscloud/create-tenant-quota-report.md) | **POST** /api/2.0/settings/docscloud/tenant/quota/report | Start the Docs Connect quota report |
| [**getTenant**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/docscloud/get-tenant.md) | **GET** /api/2.0/settings/docscloud/tenant | Get the Docs Connect tenant |
| [**getTenantConfig**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/docscloud/get-tenant-config.md) | **GET** /api/2.0/settings/docscloud/tenant/config | Get the Docs Connect tenant configuration |
| [**getTenantInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/docscloud/get-tenant-info.md) | **GET** /api/2.0/settings/docscloud/tenant/info | Get the Docs Connect tenant information |
| [**getTenantQuota**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/docscloud/get-tenant-quota.md) | **GET** /api/2.0/settings/docscloud/tenant/quota | Get the Docs Connect tenant quota |
| [**getTenantQuotaReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/docscloud/get-tenant-quota-report.md) | **GET** /api/2.0/settings/docscloud/tenant/quota/report | Get the Docs Connect quota report status |
| [**getTenantUsage**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/docscloud/get-tenant-usage.md) | **GET** /api/2.0/settings/docscloud/tenant/usage | Get the Docs Connect tenant usage |
| [**startDocsCloudTrial**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/docscloud/start-docs-cloud-trial.md) | **POST** /api/2.0/settings/docscloud/trial | Start the Docs Connect trial |
| [**switchToDevPack**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/docscloud/switch-to-dev-pack.md) | **POST** /api/2.0/settings/docscloud/switchtodevpack | Switch Docs Connect to Docs Connect Dev Pack |
| [**terminateTenantQuotaReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/docscloud/terminate-tenant-quota-report.md) | **DELETE** /api/2.0/settings/docscloud/tenant/quota/report | Terminate the Docs Connect quota report |
| [**updateTenantConfig**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/docscloud/update-tenant-config.md) | **PUT** /api/2.0/settings/docscloud/tenant/config | Update the Docs Connect tenant configuration |

## Encryption

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getStorageEncryptionProgress**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/encryption/get-storage-encryption-progress.md) | **GET** /api/2.0/settings/encryption/progress | Get the storage encryption progress |
| [**getStorageEncryptionSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/encryption/get-storage-encryption-settings.md) | **GET** /api/2.0/settings/encryption/settings | Get the storage encryption settings |
| [**startStorageEncryption**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/encryption/start-storage-encryption.md) | **POST** /api/2.0/settings/encryption/start | Start the storage encryption |

## Greeting settings

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getGreetingSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/greeting-settings/get-greeting-settings.md) | **GET** /api/2.0/settings/greetingsettings | Get greeting settings |
| [**getIsDefaultGreetingSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/greeting-settings/get-is-default-greeting-settings.md) | **GET** /api/2.0/settings/greetingsettings/isdefault | Check the default greeting settings |
| [**restoreGreetingSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/greeting-settings/restore-greeting-settings.md) | **POST** /api/2.0/settings/greetingsettings/restore | Restore the greeting settings |
| [**saveGreetingSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/greeting-settings/save-greeting-settings.md) | **POST** /api/2.0/settings/greetingsettings | Save the greeting settings |

## IP restrictions

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getIpRestrictions**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/ip-restrictions/get-ip-restrictions.md) | **GET** /api/2.0/settings/iprestrictions | Get IP restrictions |
| [**readIpRestrictionsSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/ip-restrictions/read-ip-restrictions-settings.md) | **GET** /api/2.0/settings/iprestrictions/settings | Get IP restriction settings |
| [**saveIpRestrictions**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/ip-restrictions/save-ip-restrictions.md) | **PUT** /api/2.0/settings/iprestrictions | Save IP restrictions |
| [**updateIpRestrictionsSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/ip-restrictions/update-ip-restrictions-settings.md) | **PUT** /api/2.0/settings/iprestrictions/settings | Update IP restriction settings |

## License

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**acceptLicense**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/license/accept-license.md) | **POST** /api/2.0/settings/license/accept | Activate a license |
| [**getIsLicenseRequired**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/license/get-is-license-required.md) | **GET** /api/2.0/settings/license/required | Check if a license is required |
| [**refreshLicense**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/license/refresh-license.md) | **GET** /api/2.0/settings/license/refresh | Refresh the license |
| [**uploadLicense**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/license/upload-license.md) | **POST** /api/2.0/settings/license | Upload a license |

## Login settings

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getLoginSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/login-settings/get-login-settings.md) | **GET** /api/2.0/settings/security/loginsettings | Get login settings |
| [**setDefaultLoginSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/login-settings/set-default-login-settings.md) | **DELETE** /api/2.0/settings/security/loginsettings | Reset login settings |
| [**updateLoginSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/login-settings/update-login-settings.md) | **PUT** /api/2.0/settings/security/loginsettings | Update login settings |

## Messages

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**enableAdminMessageSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/messages/enable-admin-message-settings.md) | **POST** /api/2.0/settings/messagesettings | Enable or disable administrator messages |
| [**sendAdminMail**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/messages/send-admin-mail.md) | **POST** /api/2.0/settings/sendadmmail | Send a message to the administrator |
| [**sendJoinInviteMail**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/messages/send-join-invite-mail.md) | **POST** /api/2.0/settings/sendjoininvite | Send an invitation email |

## Notifications

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getNotificationChannels**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/notifications/get-notification-channels.md) | **GET** /api/2.0/settings/notification/channels | Get notification channels |
| [**getNotificationSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/notifications/get-notification-settings.md) | **GET** /api/2.0/settings/notification/\{type\} | Check notification availability |
| [**getRoomsNotificationSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/notifications/get-rooms-notification-settings.md) | **GET** /api/2.0/settings/notification/rooms | Get muted rooms |
| [**setNotificationSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/notifications/set-notification-settings.md) | **POST** /api/2.0/settings/notification | Set notification status |
| [**setRoomsNotificationStatus**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/notifications/set-rooms-notification-status.md) | **POST** /api/2.0/settings/notification/rooms | Mute or unmute a room |

## Owner

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**sendOwnerChangeInstructions**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/owner/send-owner-change-instructions.md) | **POST** /api/2.0/settings/owner | Start the portal owner change |
| [**updatePortalOwner**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/owner/update-portal-owner.md) | **PUT** /api/2.0/settings/owner | Confirm the portal owner change |

## Quota

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getUserQuotaSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/quota/get-user-quota-settings.md) | **GET** /api/2.0/settings/userquotasettings | Get the user quota settings |
| [**saveAiAgentQuotaSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/quota/save-ai-agent-quota-settings.md) | **POST** /api/2.0/settings/aiagentquotasettings | Save the AI Agent quota settings |
| [**saveRoomQuotaSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/quota/save-room-quota-settings.md) | **POST** /api/2.0/settings/roomquotasettings | Save the room quota settings |
| [**setTenantQuotaSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/quota/set-tenant-quota-settings.md) | **PUT** /api/2.0/settings/tenantquotasettings | Save the tenant quota settings |

## Rebranding

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**deleteAdditionalWhiteLabelSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/delete-additional-white-label-settings.md) | **DELETE** /api/2.0/settings/rebranding/additional | Delete the additional white label settings |
| [**deleteCompanyWhiteLabelSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/delete-company-white-label-settings.md) | **DELETE** /api/2.0/settings/rebranding/company | Delete the company white label settings |
| [**getAdditionalWhiteLabelSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/get-additional-white-label-settings.md) | **GET** /api/2.0/settings/rebranding/additional | Get the additional white label settings |
| [**getCompanyWhiteLabelSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/get-company-white-label-settings.md) | **GET** /api/2.0/settings/rebranding/company | Get the company white label settings |
| [**getEnableWhitelabel**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/get-enable-whitelabel.md) | **GET** /api/2.0/settings/enablewhitelabel | Check the white label availability |
| [**getIsDefaultWhiteLabelLogoText**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/get-is-default-white-label-logo-text.md) | **GET** /api/2.0/settings/whitelabel/logotext/isdefault | Check the default logo text |
| [**getIsDefaultWhiteLabelLogos**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/get-is-default-white-label-logos.md) | **GET** /api/2.0/settings/whitelabel/logos/isdefault | Check the default white label logos |
| [**getLicensorData**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/get-licensor-data.md) | **GET** /api/2.0/settings/companywhitelabel | Get the licensor data |
| [**getWhiteLabelLogoText**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/get-white-label-logo-text.md) | **GET** /api/2.0/settings/whitelabel/logotext | Get the white label logo text |
| [**getWhiteLabelLogos**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/get-white-label-logos.md) | **GET** /api/2.0/settings/whitelabel/logos | Get the white label logos |
| [**restoreWhiteLabelLogoText**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/restore-white-label-logo-text.md) | **PUT** /api/2.0/settings/whitelabel/logotext/restore | Restore the white label logo text |
| [**restoreWhiteLabelLogos**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/restore-white-label-logos.md) | **PUT** /api/2.0/settings/whitelabel/logos/restore | Restore the white label logos |
| [**saveAdditionalWhiteLabelSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/save-additional-white-label-settings.md) | **POST** /api/2.0/settings/rebranding/additional | Save the additional white label settings |
| [**saveCompanyWhiteLabelSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/save-company-white-label-settings.md) | **POST** /api/2.0/settings/rebranding/company | Save the company white label settings |
| [**saveWhiteLabelLogoText**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/save-white-label-logo-text.md) | **POST** /api/2.0/settings/whitelabel/logotext/save | Save the white label logo text |
| [**saveWhiteLabelSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/save-white-label-settings.md) | **POST** /api/2.0/settings/whitelabel/logos/save | Save the white label logos |
| [**saveWhiteLabelSettingsFromFiles**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/rebranding/save-white-label-settings-from-files.md) | **POST** /api/2.0/settings/whitelabel/logos/savefromfiles | Save the logos from files |

## SSO

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getDefaultSsoSettingsV2**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/sso/get-default-sso-settings-v-2.md) | **GET** /api/2.0/settings/ssov2/default | Get the default SSO settings |
| [**getSsoSettingsV2**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/sso/get-sso-settings-v-2.md) | **GET** /api/2.0/settings/ssov2 | Get the SSO settings |
| [**getSsoSettingsV2Constants**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/sso/get-sso-settings-v-2-constants.md) | **GET** /api/2.0/settings/ssov2/constants | Get the SSO settings constants |
| [**resetSsoSettingsV2**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/sso/reset-sso-settings-v-2.md) | **DELETE** /api/2.0/settings/ssov2 | Reset the SSO settings |
| [**saveSsoSettingsV2**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/sso/save-sso-settings-v-2.md) | **POST** /api/2.0/settings/ssov2 | Save the SSO settings |

## Security

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getEnabledModules**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/security/get-enabled-modules.md) | **GET** /api/2.0/settings/security/modules | Get enabled modules |
| [**getIsProductAdministrator**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/security/get-is-product-administrator.md) | **GET** /api/2.0/settings/security/administrator | Check product administrator |
| [**getPasswordSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/security/get-password-settings.md) | **GET** /api/2.0/settings/security/password | Get password settings |
| [**getProductAdministrators**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/security/get-product-administrators.md) | **GET** /api/2.0/settings/security/administrator/\{productid\} | Get product administrators |
| [**getWebItemSecurityInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/security/get-web-item-security-info.md) | **GET** /api/2.0/settings/security/\{id\} | Check module availability |
| [**getWebItemSettingsSecurityInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/security/get-web-item-settings-security-info.md) | **GET** /api/2.0/settings/security | Get module access settings |
| [**setAccessToWebItems**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/security/set-access-to-web-items.md) | **PUT** /api/2.0/settings/security/access | Set access to modules in bulk |
| [**setProductAdministrator**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/security/set-product-administrator.md) | **PUT** /api/2.0/settings/security/administrator | Set product administrator |
| [**setWebItemSecurity**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/security/set-web-item-security.md) | **PUT** /api/2.0/settings/security | Set module access |
| [**updatePasswordSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/security/update-password-settings.md) | **PUT** /api/2.0/settings/security/password | Update password settings |

## Statistics

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getSpaceUsageStatistics**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/statistics/get-space-usage-statistics.md) | **GET** /api/2.0/settings/statistics/spaceusage/\{id\} | Get the space usage statistics |

## Storage

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getAllBackupStorages**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/storage/get-all-backup-storages.md) | **GET** /api/2.0/settings/storage/backup | Get the backup storages |
| [**getAllCdnStorages**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/storage/get-all-cdn-storages.md) | **GET** /api/2.0/settings/storage/cdn | Get the CDN storages |
| [**getAllStorages**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/storage/get-all-storages.md) | **GET** /api/2.0/settings/storage | Get the portal storages |
| [**getAmazonS3Regions**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/storage/get-amazon-s-3-regions.md) | **GET** /api/2.0/settings/storage/s3/regions | Get the Amazon S3 regions |
| [**getStorageProgress**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/storage/get-storage-progress.md) | **GET** /api/2.0/settings/storage/progress | Get the storage migration progress |
| [**resetCdnToDefault**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/storage/reset-cdn-to-default.md) | **DELETE** /api/2.0/settings/storage/cdn | Reset the CDN storage settings |
| [**resetStorageToDefault**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/storage/reset-storage-to-default.md) | **DELETE** /api/2.0/settings/storage | Reset the storage settings |
| [**updateCdnStorage**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/storage/update-cdn-storage.md) | **PUT** /api/2.0/settings/storage/cdn | Update the CDN storage |
| [**updateStorage**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/storage/update-storage.md) | **PUT** /api/2.0/settings/storage | Switch the portal storage |

## TFA settings

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getTfaAppCodes**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/tfa-settings/get-tfa-app-codes.md) | **GET** /api/2.0/settings/tfaappcodes | Get the TFA backup codes |
| [**getTfaConfirmData**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/tfa-settings/get-tfa-confirm-data.md) | **GET** /api/2.0/settings/tfaapp/confirm | Get TFA confirmation data |
| [**getTfaSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/tfa-settings/get-tfa-settings.md) | **GET** /api/2.0/settings/tfaapp | Get the TFA settings |
| [**tfaAppGenerateSetupCode**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/tfa-settings/tfa-app-generate-setup-code.md) | **GET** /api/2.0/settings/tfaapp/setup | Generate the TFA setup code |
| [**tfaValidateAuthCode**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/tfa-settings/tfa-validate-auth-code.md) | **POST** /api/2.0/settings/tfaapp/validate | Validate the TFA code |
| [**unlinkTfaApp**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/tfa-settings/unlink-tfa-app.md) | **PUT** /api/2.0/settings/tfaappnewapp | Unlink the TFA application |
| [**updateTfaAppCodes**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/tfa-settings/update-tfa-app-codes.md) | **PUT** /api/2.0/settings/tfaappnewcodes | Regenerate the TFA backup codes |
| [**updateTfaSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/tfa-settings/update-tfa-settings.md) | **PUT** /api/2.0/settings/tfaapp | Update the TFA settings |
| [**updateTfaSettingsLink**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/tfa-settings/update-tfa-settings-link.md) | **PUT** /api/2.0/settings/tfaappwithlink | Update TFA settings with a link |

## Telegram

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**checkTelegram**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/telegram/check-telegram.md) | **GET** /api/2.0/settings/telegram/check | Check the Telegram connection |
| [**linkTelegram**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/telegram/link-telegram.md) | **GET** /api/2.0/settings/telegram/link | Get the Telegram link |
| [**unlinkTelegram**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/telegram/unlink-telegram.md) | **DELETE** /api/2.0/settings/telegram/link | Unlink Telegram |

## Webhooks

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**createWebhook**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/webhooks/create-webhook.md) | **POST** /api/2.0/settings/webhook | Create a webhook |
| [**enableWebhook**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/webhooks/enable-webhook.md) | **PUT** /api/2.0/settings/webhook/enable | Switch a webhook on or off |
| [**getTenantWebhooks**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/webhooks/get-tenant-webhooks.md) | **GET** /api/2.0/settings/webhook | Get the portal webhooks |
| [**getWebhookTriggers**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/webhooks/get-webhook-triggers.md) | **GET** /api/2.0/settings/webhook/triggers | Get the webhook triggers |
| [**getWebhooksLogs**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/webhooks/get-webhooks-logs.md) | **GET** /api/2.0/settings/webhooks/log | Get the webhook delivery log |
| [**removeWebhook**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/webhooks/remove-webhook.md) | **DELETE** /api/2.0/settings/webhook/\{id\} | Remove a webhook |
| [**retryWebhook**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/webhooks/retry-webhook.md) | **PUT** /api/2.0/settings/webhook/\{id\}/retry | Retry a webhook delivery |
| [**retryWebhooks**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/webhooks/retry-webhooks.md) | **PUT** /api/2.0/settings/webhook/retry | Retry webhook deliveries |
| [**updateWebhook**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/webhooks/update-webhook.md) | **PUT** /api/2.0/settings/webhook | Update a webhook |

## Webplugins

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**addWebPluginFromFile**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/webplugins/add-web-plugin-from-file.md) | **POST** /api/2.0/settings/webplugins | Add a web plugin |
| [**deleteWebPlugin**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/webplugins/delete-web-plugin.md) | **DELETE** /api/2.0/settings/webplugins/\{name\} | Delete a web plugin |
| [**getWebPlugin**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/webplugins/get-web-plugin.md) | **GET** /api/2.0/settings/webplugins/\{name\} | Get a web plugin by name |
| [**getWebPlugins**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/webplugins/get-web-plugins.md) | **GET** /api/2.0/settings/webplugins | Get web plugins |
| [**updateWebPlugin**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/settings/webplugins/update-web-plugin.md) | **PUT** /api/2.0/settings/webplugins/\{name\} | Update a web plugin |

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

