# CurrenciesApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**defaultCurrency**](#defaultcurrency) | **POST** /v1/currencies/{code}/default | Make currency default currency.|
|[**deleteCurrency**](#deletecurrency) | **DELETE** /v1/currencies/{code} | Delete a currency.|
|[**disableCurrency**](#disablecurrency) | **POST** /v1/currencies/{code}/disable | Disable a currency.|
|[**enableCurrency**](#enablecurrency) | **POST** /v1/currencies/{code}/enable | Enable a single currency.|
|[**getCurrency**](#getcurrency) | **GET** /v1/currencies/{code} | Get a single currency.|
|[**getNativeCurrency**](#getnativecurrency) | **GET** /v1/currencies/native | Get the native currency of the current administration.|
|[**listAccountByCurrency**](#listaccountbycurrency) | **GET** /v1/currencies/{code}/accounts | List all accounts with this currency.|
|[**listAvailableBudgetByCurrency**](#listavailablebudgetbycurrency) | **GET** /v1/currencies/{code}/available-budgets | List all available budgets with this currency.|
|[**listBillByCurrency**](#listbillbycurrency) | **GET** /v1/currencies/{code}/bills | List all bills with this currency.|
|[**listBudgetLimitByCurrency**](#listbudgetlimitbycurrency) | **GET** /v1/currencies/{code}/budget-limits | List all budget limits with this currency|
|[**listCurrency**](#listcurrency) | **GET** /v1/currencies | List all currencies.|
|[**listRecurrenceByCurrency**](#listrecurrencebycurrency) | **GET** /v1/currencies/{code}/recurrences | List all recurring transactions with this currency.|
|[**listRuleByCurrency**](#listrulebycurrency) | **GET** /v1/currencies/{code}/rules | List all rules with this currency.|
|[**listTransactionByCurrency**](#listtransactionbycurrency) | **GET** /v1/currencies/{code}/transactions | List all transactions with this currency.|
|[**storeCurrency**](#storecurrency) | **POST** /v1/currencies | Store a new currency|
|[**updateCurrency**](#updatecurrency) | **PUT** /v1/currencies/{code} | Update existing currency.|

# **defaultCurrency**
> CurrencySingle defaultCurrency()

Make this currency the default currency for the user. If the currency is not enabled, it will be enabled as well.

### Example

```typescript
import {
    CurrenciesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrenciesApi(configuration);

let code: string; //The currency code. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.defaultCurrency(
    code,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **code** | [**string**] | The currency code. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**CurrencySingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**204** | Currency has been made the default currency. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteCurrency**
> deleteCurrency()

Delete a currency.

### Example

```typescript
import {
    CurrenciesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrenciesApi(configuration);

let code: string; //The currency code. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.deleteCurrency(
    code,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **code** | [**string**] | The currency code. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

void (empty response body)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**204** | Currency deleted. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **disableCurrency**
> CurrencySingle disableCurrency()

Disable a currency.

### Example

```typescript
import {
    CurrenciesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrenciesApi(configuration);

let code: string; //The currency code. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.disableCurrency(
    code,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **code** | [**string**] | The currency code. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**CurrencySingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**204** | Currency was disabled. |  -  |
|**409** | Currency cannot be disabled, because it is still in use. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enableCurrency**
> CurrencySingle enableCurrency()

Enable a single currency.

### Example

```typescript
import {
    CurrenciesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrenciesApi(configuration);

let code: string; //The currency code. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.enableCurrency(
    code,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **code** | [**string**] | The currency code. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**CurrencySingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**204** | Currency was enabled. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getCurrency**
> CurrencySingle getCurrency()

Get a single currency.

### Example

```typescript
import {
    CurrenciesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrenciesApi(configuration);

let code: string; //The currency code. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getCurrency(
    code,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **code** | [**string**] | The currency code. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**CurrencySingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The requested currency |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getNativeCurrency**
> CurrencySingle getNativeCurrency()

Get the native currency of the current administration. This replaces what was called \"the user\'s default currency\" although they are essentially the same.

### Example

```typescript
import {
    CurrenciesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrenciesApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getNativeCurrency(
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**CurrencySingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The native currency |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listAccountByCurrency**
> AccountArray listAccountByCurrency()

List all accounts with this currency.

### Example

```typescript
import {
    CurrenciesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrenciesApi(configuration);

let code: string; //The currency code. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)
let date: string; //A date formatted YYYY-MM-DD. When added to the request, Firefly III will show the account\'s balance on that day.  (optional) (default to undefined)
let type: AccountTypeFilter; //Optional filter on the account type(s) returned (optional) (default to undefined)

const { status, data } = await apiInstance.listAccountByCurrency(
    code,
    xTraceId,
    limit,
    page,
    date,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **code** | [**string**] | The currency code. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|
| **date** | [**string**] | A date formatted YYYY-MM-DD. When added to the request, Firefly III will show the account\&#39;s balance on that day.  | (optional) defaults to undefined|
| **type** | **AccountTypeFilter** | Optional filter on the account type(s) returned | (optional) defaults to undefined|


### Return type

**AccountArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of accounts |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listAvailableBudgetByCurrency**
> AvailableBudgetArray listAvailableBudgetByCurrency()

List all available budgets with this currency.

### Example

```typescript
import {
    CurrenciesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrenciesApi(configuration);

let code: string; //The currency code. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listAvailableBudgetByCurrency(
    code,
    xTraceId,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **code** | [**string**] | The currency code. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|


### Return type

**AvailableBudgetArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of available budgets |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listBillByCurrency**
> BillArray listBillByCurrency()

List all bills with this currency.

### Example

```typescript
import {
    CurrenciesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrenciesApi(configuration);

let code: string; //The currency code. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listBillByCurrency(
    code,
    xTraceId,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **code** | [**string**] | The currency code. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|


### Return type

**BillArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of bills. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listBudgetLimitByCurrency**
> BudgetLimitArray listBudgetLimitByCurrency()

List all budget limits with this currency

### Example

```typescript
import {
    CurrenciesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrenciesApi(configuration);

let code: string; //The currency code. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)
let start: string; //Start date for the budget limit list. (optional) (default to undefined)
let end: string; //End date for the budget limit list. (optional) (default to undefined)

const { status, data } = await apiInstance.listBudgetLimitByCurrency(
    code,
    xTraceId,
    limit,
    page,
    start,
    end
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **code** | [**string**] | The currency code. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|
| **start** | [**string**] | Start date for the budget limit list. | (optional) defaults to undefined|
| **end** | [**string**] | End date for the budget limit list. | (optional) defaults to undefined|


### Return type

**BudgetLimitArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of budget limits. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listCurrency**
> CurrencyArray listCurrency()

List all currencies.

### Example

```typescript
import {
    CurrenciesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrenciesApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listCurrency(
    xTraceId,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|


### Return type

**CurrencyArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of currencies. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listRecurrenceByCurrency**
> RecurrenceArray listRecurrenceByCurrency()

List all recurring transactions with this currency.

### Example

```typescript
import {
    CurrenciesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrenciesApi(configuration);

let code: string; //The currency code. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listRecurrenceByCurrency(
    code,
    xTraceId,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **code** | [**string**] | The currency code. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|


### Return type

**RecurrenceArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of recurring transactions |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listRuleByCurrency**
> RuleArray listRuleByCurrency()

List all rules with this currency.

### Example

```typescript
import {
    CurrenciesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrenciesApi(configuration);

let code: string; //The currency code. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listRuleByCurrency(
    code,
    xTraceId,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **code** | [**string**] | The currency code. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|


### Return type

**RuleArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of rules |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listTransactionByCurrency**
> TransactionArray listTransactionByCurrency()

List all transactions with this currency.

### Example

```typescript
import {
    CurrenciesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrenciesApi(configuration);

let code: string; //The currency code. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)
let start: string; //A date formatted YYYY-MM-DD, to limit the list of transactions.  (optional) (default to undefined)
let end: string; //A date formatted YYYY-MM-DD, to limit the list of transactions.  (optional) (default to undefined)
let type: TransactionTypeFilter; //Optional filter on the transaction type(s) returned (optional) (default to undefined)

const { status, data } = await apiInstance.listTransactionByCurrency(
    code,
    xTraceId,
    limit,
    page,
    start,
    end,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **code** | [**string**] | The currency code. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|
| **start** | [**string**] | A date formatted YYYY-MM-DD, to limit the list of transactions.  | (optional) defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD, to limit the list of transactions.  | (optional) defaults to undefined|
| **type** | **TransactionTypeFilter** | Optional filter on the transaction type(s) returned | (optional) defaults to undefined|


### Return type

**TransactionArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of transactions. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **storeCurrency**
> CurrencySingle storeCurrency(currencyStore)

Creates a new currency. The data required can be submitted as a JSON body or as a list of parameters.

### Example

```typescript
import {
    CurrenciesApi,
    Configuration,
    CurrencyStore
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrenciesApi(configuration);

let currencyStore: CurrencyStore; //JSON array or key=value pairs with the necessary currency information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.storeCurrency(
    currencyStore,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **currencyStore** | **CurrencyStore**| JSON array or key&#x3D;value pairs with the necessary currency information. See the model for the exact specifications. | |
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**CurrencySingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | New currency stored, result in response. |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateCurrency**
> CurrencySingle updateCurrency(currencyUpdate)

Update existing currency.

### Example

```typescript
import {
    CurrenciesApi,
    Configuration,
    CurrencyUpdate
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrenciesApi(configuration);

let code: string; //The currency code. (default to undefined)
let currencyUpdate: CurrencyUpdate; //JSON array with updated currency information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.updateCurrency(
    code,
    currencyUpdate,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **currencyUpdate** | **CurrencyUpdate**| JSON array with updated currency information. See the model for the exact specifications. | |
| **code** | [**string**] | The currency code. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**CurrencySingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/vnd.api+json, application/x-www-form-urlencoded
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Updated currency stored, result in response |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

