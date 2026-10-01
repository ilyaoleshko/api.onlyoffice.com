# ONLYOFFICE DocSpace Portal API

The browsable version of this reference, with a request builder and code samples, is published at
[https://api.onlyoffice.com/docspace/api-backend/usage-api/](https://api.onlyoffice.com/docspace/api-backend/usage-api/).

All URIs are relative to *https://yourportal.onlyoffice.com*, where the host is the address of your DocSpace instance.

## Guests

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getGuestSharingLink**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/guests/get-guest-sharing-link.md) | **GET** /api/2.0/people/guests/\{userid\}/share | Get a guest sharing link |

## Payment

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**calculateWalletPayment**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/calculate-wallet-payment.md) | **PUT** /api/2.0/portal/payment/calculatewallet | Calculate the wallet payment amount |
| [**changeTenantWalletServiceState**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/change-tenant-wallet-service-state.md) | **POST** /api/2.0/portal/payment/servicestate | Switch a wallet service |
| [**createCustomerMonthlyUsageReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/create-customer-monthly-usage-report.md) | **POST** /api/2.0/portal/payment/customer/usage/monthly/report | Start the monthly usage report |
| [**createCustomerOperationsReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/create-customer-operations-report.md) | **POST** /api/2.0/portal/payment/customer/operationsreport | Start the operations report |
| [**createCustomerServiceUsageReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/create-customer-service-usage-report.md) | **POST** /api/2.0/portal/payment/customer/usage/report | Start the service usage report |
| [**getAccountingServicePrices**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-accounting-service-prices.md) | **GET** /api/2.0/portal/payment/accounting/prices/\{serviceName\} | Get the service prices from the accounting service |
| [**getActiveServices**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-active-services.md) | **GET** /api/2.0/portal/payment/activeservices | Get the active wallet services |
| [**getAiPrices**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-ai-prices.md) | **GET** /api/2.0/portal/payment/ai-prices | Get AI model prices |
| [**getCheckoutSetupUrl**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-checkout-setup-url.md) | **GET** /api/2.0/portal/payment/checkoutsetupurl | Get the checkout setup page URL |
| [**getCustomerBalance**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-customer-balance.md) | **GET** /api/2.0/portal/payment/customer/balance | Get the customer balance |
| [**getCustomerInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-customer-info.md) | **GET** /api/2.0/portal/payment/customerinfo | Get the customer information |
| [**getCustomerMonthlyUsage**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-customer-monthly-usage.md) | **GET** /api/2.0/portal/payment/customer/usage/monthly | Get the customer monthly usage |
| [**getCustomerMonthlyUsageReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-customer-monthly-usage-report.md) | **GET** /api/2.0/portal/payment/customer/usage/monthly/report | Get the monthly usage report status |
| [**getCustomerOperations**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-customer-operations.md) | **GET** /api/2.0/portal/payment/customer/operations | Get the wallet operations |
| [**getCustomerOperationsReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-customer-operations-report.md) | **GET** /api/2.0/portal/payment/customer/operationsreport | Get the operations report status |
| [**getCustomerServiceUsage**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-customer-service-usage.md) | **GET** /api/2.0/portal/payment/customer/usage | Get the customer service usage |
| [**getCustomerServiceUsageReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-customer-service-usage-report.md) | **GET** /api/2.0/portal/payment/customer/usage/report | Get the service usage report status |
| [**getPaymentAccount**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-payment-account.md) | **GET** /api/2.0/portal/payment/account | Get the billing account page |
| [**getPaymentCurrencies**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-payment-currencies.md) | **GET** /api/2.0/portal/payment/currencies | Get the billing currencies |
| [**getPaymentQuotas**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-payment-quotas.md) | **GET** /api/2.0/portal/payment/quotas | Get the purchasable quotas |
| [**getPaymentUrl**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-payment-url.md) | **PUT** /api/2.0/portal/payment/url | Get the payment page URL |
| [**getPortalPrices**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-portal-prices.md) | **GET** /api/2.0/portal/payment/prices | Get the product prices |
| [**getQuotaPaymentInformation**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-quota-payment-information.md) | **GET** /api/2.0/portal/payment/quota | Get the current plan and limits |
| [**getRestrictedAiModels**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-restricted-ai-models.md) | **GET** /api/2.0/portal/payment/ai-model/restrictions | Get restricted AI models |
| [**getSubscriptionBalanceInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-subscription-balance-info.md) | **GET** /api/2.0/portal/payment/subscription/balance | Get the subscription balance information |
| [**getTenantWalletServiceSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-tenant-wallet-service-settings.md) | **GET** /api/2.0/portal/payment/servicessettings | Get the wallet service settings |
| [**getTenantWalletSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-tenant-wallet-settings.md) | **GET** /api/2.0/portal/payment/topupsettings | Get the auto top-up settings |
| [**getWalletService**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-wallet-service.md) | **GET** /api/2.0/portal/payment/walletservice | Get a wallet service |
| [**getWalletServices**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/get-wallet-services.md) | **GET** /api/2.0/portal/payment/walletservices | Get wallet services |
| [**moveSubscriptionToWallet**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/move-subscription-to-wallet.md) | **POST** /api/2.0/portal/payment/subscription/movetowallet | Move the subscription to the wallet |
| [**sendPaymentRequest**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/send-payment-request.md) | **POST** /api/2.0/portal/payment/request | Contact the sales team |
| [**setRestrictedAiModels**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/set-restricted-ai-models.md) | **PUT** /api/2.0/portal/payment/ai-model/restrictions | Set restricted AI models |
| [**setTenantWalletSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/set-tenant-wallet-settings.md) | **POST** /api/2.0/portal/payment/topupsettings | Set the auto top-up settings |
| [**terminateCustomerMonthlyUsageReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/terminate-customer-monthly-usage-report.md) | **DELETE** /api/2.0/portal/payment/customer/usage/monthly/report | Terminate the monthly usage report |
| [**terminateCustomerOperationsReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/terminate-customer-operations-report.md) | **DELETE** /api/2.0/portal/payment/customer/operationsreport | Terminate the operations report |
| [**terminateCustomerServiceUsageReport**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/terminate-customer-service-usage-report.md) | **DELETE** /api/2.0/portal/payment/customer/usage/report | Terminate the service usage report |
| [**topUpDeposit**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/top-up-deposit.md) | **POST** /api/2.0/portal/payment/deposit | Top up the wallet |
| [**updatePayment**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/update-payment.md) | **PUT** /api/2.0/portal/payment/update | Change the subscription quantity |
| [**updateWalletPayment**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/payment/update-wallet-payment.md) | **PUT** /api/2.0/portal/payment/updatewallet | Change a wallet service quantity |

## Quota

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**getPortalQuota**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/quota/get-portal-quota.md) | **GET** /api/2.0/portal/quota | Get the portal quota |
| [**getPortalTariff**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/quota/get-portal-tariff.md) | **GET** /api/2.0/portal/tariff | Get the portal tariff |
| [**getPortalUsedSpace**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/quota/get-portal-used-space.md) | **GET** /api/2.0/portal/usedspace | Get the portal used space |
| [**getRightQuota**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/quota/get-right-quota.md) | **GET** /api/2.0/portal/quota/right | Get the recommended quota |
| [**getUpcomingPayments**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/quota/get-upcoming-payments.md) | **GET** /api/2.0/portal/tariff/upcoming | Get upcoming payments |

## Settings

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**continuePortal**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/settings/continue-portal.md) | **PUT** /api/2.0/portal/continue | Restore a portal |
| [**deletePortal**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/settings/delete-portal.md) | **DELETE** /api/2.0/portal/delete | Delete a portal |
| [**getPortalInformation**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/settings/get-portal-information.md) | **GET** /api/2.0/portal | Get portal information |
| [**getPortalPath**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/settings/get-portal-path.md) | **GET** /api/2.0/portal/path | Get a path to the portal |
| [**sendDeleteInstructions**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/settings/send-delete-instructions.md) | **POST** /api/2.0/portal/delete | Send removal instructions |
| [**sendSuspendInstructions**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/settings/send-suspend-instructions.md) | **POST** /api/2.0/portal/suspend | Send suspension instructions |
| [**suspendPortal**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/settings/suspend-portal.md) | **PUT** /api/2.0/portal/suspend | Deactivate a portal |

## Users

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**createInvitationLink**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/users/create-invitation-link.md) | **POST** /api/2.0/portal/users/invitationlink | Create an invitation link |
| [**deleteInvitationLink**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/users/delete-invitation-link.md) | **DELETE** /api/2.0/portal/users/invitationlink | Delete an invitation link |
| [**getInvitationLink**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/users/get-invitation-link.md) | **GET** /api/2.0/portal/users/invite/\{employeeType\} | Get a legacy invitation link |
| [**getInvitationLinkByEmployeeType**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/users/get-invitation-link-by-employee-type.md) | **GET** /api/2.0/portal/users/invitationlink/\{employeeType\} | Get an invitation link by role |
| [**getPortalUsersCount**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/users/get-portal-users-count.md) | **GET** /api/2.0/portal/userscount | Get a number of portal users |
| [**getUserById**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/users/get-user-by-id.md) | **GET** /api/2.0/portal/users/\{userID\} | Get a portal user |
| [**markGiftMessageAsRead**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/users/mark-gift-message-as-read.md) | **POST** /api/2.0/portal/present/mark | Mark a gift message as read |
| [**sendCongratulations**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/users/send-congratulations.md) | **POST** /api/2.0/portal/sendcongratulations | Send congratulations |
| [**updateInvitationLink**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/portal/users/update-invitation-link.md) | **PUT** /api/2.0/portal/users/invitationlink | Update an invitation link |

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

