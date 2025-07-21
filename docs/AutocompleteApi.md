# AutocompleteApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getAccountsAC**](#getaccountsac) | **GET** /v1/autocomplete/accounts | Returns all accounts of the user returned in a basic auto-complete array.|
|[**getBillsAC**](#getbillsac) | **GET** /v1/autocomplete/bills | Returns all bills of the user returned in a basic auto-complete array.|
|[**getBudgetsAC**](#getbudgetsac) | **GET** /v1/autocomplete/budgets | Returns all budgets of the user returned in a basic auto-complete array.|
|[**getCategoriesAC**](#getcategoriesac) | **GET** /v1/autocomplete/categories | Returns all categories of the user returned in a basic auto-complete array.|
|[**getCurrenciesAC**](#getcurrenciesac) | **GET** /v1/autocomplete/currencies | Returns all currencies of the user returned in a basic auto-complete array.|
|[**getCurrenciesCodeAC**](#getcurrenciescodeac) | **GET** /v1/autocomplete/currencies-with-code | Returns all currencies of the user returned in a basic auto-complete array. This endpoint is DEPRECATED and I suggest you DO NOT use it.|
|[**getObjectGroupsAC**](#getobjectgroupsac) | **GET** /v1/autocomplete/object-groups | Returns all object groups of the user returned in a basic auto-complete array.|
|[**getPiggiesAC**](#getpiggiesac) | **GET** /v1/autocomplete/piggy-banks | Returns all piggy banks of the user returned in a basic auto-complete array.|
|[**getPiggiesBalanceAC**](#getpiggiesbalanceac) | **GET** /v1/autocomplete/piggy-banks-with-balance | Returns all piggy banks of the user returned in a basic auto-complete array.|
|[**getRecurringAC**](#getrecurringac) | **GET** /v1/autocomplete/recurring | Returns all recurring transactions of the user returned in a basic auto-complete array.|
|[**getRuleGroupsAC**](#getrulegroupsac) | **GET** /v1/autocomplete/rule-groups | Returns all rule groups of the user returned in a basic auto-complete array.|
|[**getRulesAC**](#getrulesac) | **GET** /v1/autocomplete/rules | Returns all rules of the user returned in a basic auto-complete array.|
|[**getTagAC**](#gettagac) | **GET** /v1/autocomplete/tags | Returns all tags of the user returned in a basic auto-complete array.|
|[**getTransactionTypesAC**](#gettransactiontypesac) | **GET** /v1/autocomplete/transaction-types | Returns all transaction types returned in a basic auto-complete array. English only.|
|[**getTransactionsAC**](#gettransactionsac) | **GET** /v1/autocomplete/transactions | Returns all transaction descriptions of the user returned in a basic auto-complete array.|
|[**getTransactionsIDAC**](#gettransactionsidac) | **GET** /v1/autocomplete/transactions-with-id | Returns all transactions, complemented with their ID, of the user returned in a basic auto-complete array. This endpoint is DEPRECATED and I suggest you DO NOT use it.|

# **getAccountsAC**
> Array<AutocompleteAccount> getAccountsAC()


### Example

```typescript
import {
    AutocompleteApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AutocompleteApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let query: string; //The autocomplete search query. (optional) (default to undefined)
let limit: number; //The number of items returned. (optional) (default to undefined)
let date: string; //If the account is an asset account or a liability, the autocomplete will also return the balance of the account on this date. (optional) (default to undefined)
let types: Array<AccountTypeFilter>; //Optional filter on the account type(s) used in the autocomplete. (optional) (default to undefined)

const { status, data } = await apiInstance.getAccountsAC(
    xTraceId,
    query,
    limit,
    date,
    types
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **query** | [**string**] | The autocomplete search query. | (optional) defaults to undefined|
| **limit** | [**number**] | The number of items returned. | (optional) defaults to undefined|
| **date** | [**string**] | If the account is an asset account or a liability, the autocomplete will also return the balance of the account on this date. | (optional) defaults to undefined|
| **types** | **Array&lt;AccountTypeFilter&gt;** | Optional filter on the account type(s) used in the autocomplete. | (optional) defaults to undefined|


### Return type

**Array<AutocompleteAccount>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | A list of accounts with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getBillsAC**
> Array<AutocompleteBill> getBillsAC()


### Example

```typescript
import {
    AutocompleteApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AutocompleteApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let query: string; //The autocomplete search query. (optional) (default to undefined)
let limit: number; //The number of items returned. (optional) (default to undefined)

const { status, data } = await apiInstance.getBillsAC(
    xTraceId,
    query,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **query** | [**string**] | The autocomplete search query. | (optional) defaults to undefined|
| **limit** | [**number**] | The number of items returned. | (optional) defaults to undefined|


### Return type

**Array<AutocompleteBill>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**500** | Internal exception |  -  |
|**200** | A list of bills with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getBudgetsAC**
> Array<AutocompleteBudget> getBudgetsAC()


### Example

```typescript
import {
    AutocompleteApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AutocompleteApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let query: string; //The autocomplete search query. (optional) (default to undefined)
let limit: number; //The number of items returned. (optional) (default to undefined)

const { status, data } = await apiInstance.getBudgetsAC(
    xTraceId,
    query,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **query** | [**string**] | The autocomplete search query. | (optional) defaults to undefined|
| **limit** | [**number**] | The number of items returned. | (optional) defaults to undefined|


### Return type

**Array<AutocompleteBudget>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**200** | A list of budgets with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getCategoriesAC**
> Array<AutocompleteCategory> getCategoriesAC()


### Example

```typescript
import {
    AutocompleteApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AutocompleteApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let query: string; //The autocomplete search query. (optional) (default to undefined)
let limit: number; //The number of items returned. (optional) (default to undefined)

const { status, data } = await apiInstance.getCategoriesAC(
    xTraceId,
    query,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **query** | [**string**] | The autocomplete search query. | (optional) defaults to undefined|
| **limit** | [**number**] | The number of items returned. | (optional) defaults to undefined|


### Return type

**Array<AutocompleteCategory>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**500** | Internal exception |  -  |
|**200** | A list of categories with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getCurrenciesAC**
> Array<AutocompleteCurrency> getCurrenciesAC()


### Example

```typescript
import {
    AutocompleteApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AutocompleteApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let query: string; //The autocomplete search query. (optional) (default to undefined)
let limit: number; //The number of items returned. (optional) (default to undefined)

const { status, data } = await apiInstance.getCurrenciesAC(
    xTraceId,
    query,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **query** | [**string**] | The autocomplete search query. | (optional) defaults to undefined|
| **limit** | [**number**] | The number of items returned. | (optional) defaults to undefined|


### Return type

**Array<AutocompleteCurrency>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**200** | A list of currencies with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getCurrenciesCodeAC**
> Array<AutocompleteCurrencyCode> getCurrenciesCodeAC()


### Example

```typescript
import {
    AutocompleteApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AutocompleteApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let query: string; //The autocomplete search query. (optional) (default to undefined)
let limit: number; //The number of items returned. (optional) (default to undefined)

const { status, data } = await apiInstance.getCurrenciesCodeAC(
    xTraceId,
    query,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **query** | [**string**] | The autocomplete search query. | (optional) defaults to undefined|
| **limit** | [**number**] | The number of items returned. | (optional) defaults to undefined|


### Return type

**Array<AutocompleteCurrencyCode>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | A list of currencies with very basic information and the currency code between brackets. This endpoint is DEPRECATED and I suggest you DO NOT use it. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getObjectGroupsAC**
> Array<AutocompleteObjectGroup> getObjectGroupsAC()


### Example

```typescript
import {
    AutocompleteApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AutocompleteApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let query: string; //The autocomplete search query. (optional) (default to undefined)
let limit: number; //The number of items returned. (optional) (default to undefined)

const { status, data } = await apiInstance.getObjectGroupsAC(
    xTraceId,
    query,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **query** | [**string**] | The autocomplete search query. | (optional) defaults to undefined|
| **limit** | [**number**] | The number of items returned. | (optional) defaults to undefined|


### Return type

**Array<AutocompleteObjectGroup>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**200** | A list of object groups with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPiggiesAC**
> Array<AutocompletePiggy> getPiggiesAC()


### Example

```typescript
import {
    AutocompleteApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AutocompleteApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let query: string; //The autocomplete search query. (optional) (default to undefined)
let limit: number; //The number of items returned. (optional) (default to undefined)

const { status, data } = await apiInstance.getPiggiesAC(
    xTraceId,
    query,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **query** | [**string**] | The autocomplete search query. | (optional) defaults to undefined|
| **limit** | [**number**] | The number of items returned. | (optional) defaults to undefined|


### Return type

**Array<AutocompletePiggy>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**200** | A list of piggy banks with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPiggiesBalanceAC**
> Array<AutocompletePiggyBalance> getPiggiesBalanceAC()


### Example

```typescript
import {
    AutocompleteApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AutocompleteApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let query: string; //The autocomplete search query. (optional) (default to undefined)
let limit: number; //The number of items returned. (optional) (default to undefined)

const { status, data } = await apiInstance.getPiggiesBalanceAC(
    xTraceId,
    query,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **query** | [**string**] | The autocomplete search query. | (optional) defaults to undefined|
| **limit** | [**number**] | The number of items returned. | (optional) defaults to undefined|


### Return type

**Array<AutocompletePiggyBalance>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | A list of piggy banks with very basic balance information. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getRecurringAC**
> Array<AutocompleteRecurrence> getRecurringAC()


### Example

```typescript
import {
    AutocompleteApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AutocompleteApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let query: string; //The autocomplete search query. (optional) (default to undefined)
let limit: number; //The number of items returned. (optional) (default to undefined)

const { status, data } = await apiInstance.getRecurringAC(
    xTraceId,
    query,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **query** | [**string**] | The autocomplete search query. | (optional) defaults to undefined|
| **limit** | [**number**] | The number of items returned. | (optional) defaults to undefined|


### Return type

**Array<AutocompleteRecurrence>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**200** | A list of recurring transactions with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getRuleGroupsAC**
> Array<AutocompleteRuleGroup> getRuleGroupsAC()


### Example

```typescript
import {
    AutocompleteApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AutocompleteApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let query: string; //The autocomplete search query. (optional) (default to undefined)
let limit: number; //The number of items returned. (optional) (default to undefined)

const { status, data } = await apiInstance.getRuleGroupsAC(
    xTraceId,
    query,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **query** | [**string**] | The autocomplete search query. | (optional) defaults to undefined|
| **limit** | [**number**] | The number of items returned. | (optional) defaults to undefined|


### Return type

**Array<AutocompleteRuleGroup>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**200** | A list of rule groups with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getRulesAC**
> Array<AutocompleteRule> getRulesAC()


### Example

```typescript
import {
    AutocompleteApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AutocompleteApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let query: string; //The autocomplete search query. (optional) (default to undefined)
let limit: number; //The number of items returned. (optional) (default to undefined)

const { status, data } = await apiInstance.getRulesAC(
    xTraceId,
    query,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **query** | [**string**] | The autocomplete search query. | (optional) defaults to undefined|
| **limit** | [**number**] | The number of items returned. | (optional) defaults to undefined|


### Return type

**Array<AutocompleteRule>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**200** | A list of rules with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getTagAC**
> Array<AutocompleteTag> getTagAC()


### Example

```typescript
import {
    AutocompleteApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AutocompleteApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let query: string; //The autocomplete search query. (optional) (default to undefined)
let limit: number; //The number of items returned. (optional) (default to undefined)

const { status, data } = await apiInstance.getTagAC(
    xTraceId,
    query,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **query** | [**string**] | The autocomplete search query. | (optional) defaults to undefined|
| **limit** | [**number**] | The number of items returned. | (optional) defaults to undefined|


### Return type

**Array<AutocompleteTag>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | A list of tags with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getTransactionTypesAC**
> Array<AutocompleteTransactionType> getTransactionTypesAC()


### Example

```typescript
import {
    AutocompleteApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AutocompleteApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let query: string; //The autocomplete search query. (optional) (default to undefined)
let limit: number; //The number of items returned. (optional) (default to undefined)

const { status, data } = await apiInstance.getTransactionTypesAC(
    xTraceId,
    query,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **query** | [**string**] | The autocomplete search query. | (optional) defaults to undefined|
| **limit** | [**number**] | The number of items returned. | (optional) defaults to undefined|


### Return type

**Array<AutocompleteTransactionType>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | A list of transaction types with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getTransactionsAC**
> Array<AutocompleteTransaction> getTransactionsAC()


### Example

```typescript
import {
    AutocompleteApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AutocompleteApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let query: string; //The autocomplete search query. (optional) (default to undefined)
let limit: number; //The number of items returned. (optional) (default to undefined)

const { status, data } = await apiInstance.getTransactionsAC(
    xTraceId,
    query,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **query** | [**string**] | The autocomplete search query. | (optional) defaults to undefined|
| **limit** | [**number**] | The number of items returned. | (optional) defaults to undefined|


### Return type

**Array<AutocompleteTransaction>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | A list of transaction descriptions with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getTransactionsIDAC**
> Array<AutocompleteTransactionID> getTransactionsIDAC()


### Example

```typescript
import {
    AutocompleteApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AutocompleteApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let query: string; //The autocomplete search query. (optional) (default to undefined)
let limit: number; //The number of items returned. (optional) (default to undefined)

const { status, data } = await apiInstance.getTransactionsIDAC(
    xTraceId,
    query,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **query** | [**string**] | The autocomplete search query. | (optional) defaults to undefined|
| **limit** | [**number**] | The number of items returned. | (optional) defaults to undefined|


### Return type

**Array<AutocompleteTransactionID>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | A list of transactions with very basic information. This endpoint is DEPRECATED and I suggest you DO NOT use it. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

