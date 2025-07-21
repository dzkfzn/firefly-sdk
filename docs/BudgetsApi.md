# BudgetsApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteBudget**](#deletebudget) | **DELETE** /v1/budgets/{id} | Delete a budget.|
|[**deleteBudgetLimit**](#deletebudgetlimit) | **DELETE** /v1/budgets/{id}/limits/{limitId} | Delete a budget limit.|
|[**getBudget**](#getbudget) | **GET** /v1/budgets/{id} | Get a single budget.|
|[**getBudgetLimit**](#getbudgetlimit) | **GET** /v1/budgets/{id}/limits/{limitId} | Get single budget limit.|
|[**listAttachmentByBudget**](#listattachmentbybudget) | **GET** /v1/budgets/{id}/attachments | Lists all attachments of a budget.|
|[**listBudget**](#listbudget) | **GET** /v1/budgets | List all budgets.|
|[**listBudgetLimit**](#listbudgetlimit) | **GET** /v1/budget-limits | Get list of budget limits by date|
|[**listBudgetLimitByBudget**](#listbudgetlimitbybudget) | **GET** /v1/budgets/{id}/limits | Get all limits for a budget.|
|[**listTransactionByBudget**](#listtransactionbybudget) | **GET** /v1/budgets/{id}/transactions | All transactions to a budget.|
|[**listTransactionByBudgetLimit**](#listtransactionbybudgetlimit) | **GET** /v1/budgets/{id}/limits/{limitId}/transactions | List all transactions by a budget limit ID.|
|[**listTransactionWithoutBudget**](#listtransactionwithoutbudget) | **GET** /v1/budgets/transactions-without-budget | All transactions without a budget.|
|[**storeBudget**](#storebudget) | **POST** /v1/budgets | Store a new budget|
|[**storeBudgetLimit**](#storebudgetlimit) | **POST** /v1/budgets/{id}/limits | Store new budget limit.|
|[**updateBudget**](#updatebudget) | **PUT** /v1/budgets/{id} | Update existing budget.|
|[**updateBudgetLimit**](#updatebudgetlimit) | **PUT** /v1/budgets/{id}/limits/{limitId} | Update existing budget limit.|

# **deleteBudget**
> deleteBudget()

Delete a budget. Transactions will not be deleted.

### Example

```typescript
import {
    BudgetsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BudgetsApi(configuration);

let id: string; //The ID of the budget. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.deleteBudget(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the budget. | defaults to undefined|
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
|**204** | Budget deleted. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteBudgetLimit**
> deleteBudgetLimit()

Delete a budget limit.

### Example

```typescript
import {
    BudgetsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BudgetsApi(configuration);

let id: string; //The ID of the budget. The budget limit MUST be associated to the budget ID. (default to undefined)
let limitId: string; //The ID of the budget limit. The budget limit MUST be associated to the budget ID. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.deleteBudgetLimit(
    id,
    limitId,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the budget. The budget limit MUST be associated to the budget ID. | defaults to undefined|
| **limitId** | [**string**] | The ID of the budget limit. The budget limit MUST be associated to the budget ID. | defaults to undefined|
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
|**204** | Budget limit deleted. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getBudget**
> BudgetSingle getBudget()

Get a single budget. If the start date and end date are submitted as well, the \"spent\" array will be updated accordingly.

### Example

```typescript
import {
    BudgetsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BudgetsApi(configuration);

let id: string; //The ID of the requested budget. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let start: string; //A date formatted YYYY-MM-DD, to get info on how much the user has spent.  (optional) (default to undefined)
let end: string; //A date formatted YYYY-MM-DD, to get info on how much the user has spent.  (optional) (default to undefined)

const { status, data } = await apiInstance.getBudget(
    id,
    xTraceId,
    start,
    end
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the requested budget. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **start** | [**string**] | A date formatted YYYY-MM-DD, to get info on how much the user has spent.  | (optional) defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD, to get info on how much the user has spent.  | (optional) defaults to undefined|


### Return type

**BudgetSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The requested budget |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getBudgetLimit**
> BudgetLimitSingle getBudgetLimit()


### Example

```typescript
import {
    BudgetsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BudgetsApi(configuration);

let id: string; //The ID of the budget. The budget limit MUST be associated to the budget ID. (default to undefined)
let limitId: number; //The ID of the budget limit. The budget limit MUST be associated to the budget ID. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getBudgetLimit(
    id,
    limitId,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the budget. The budget limit MUST be associated to the budget ID. | defaults to undefined|
| **limitId** | [**number**] | The ID of the budget limit. The budget limit MUST be associated to the budget ID. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**BudgetLimitSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The requested budget limit |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listAttachmentByBudget**
> AttachmentArray listAttachmentByBudget()

Lists all attachments.

### Example

```typescript
import {
    BudgetsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BudgetsApi(configuration);

let id: string; //The ID of the budget. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listAttachmentByBudget(
    id,
    xTraceId,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the budget. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|


### Return type

**AttachmentArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of attachments |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listBudget**
> BudgetArray listBudget()

List all the budgets the user has made. If the start date and end date are submitted as well, the \"spent\" array will be updated accordingly.

### Example

```typescript
import {
    BudgetsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BudgetsApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)
let start: string; //A date formatted YYYY-MM-DD, to get info on how much the user has spent. You must submit both start and end.  (optional) (default to undefined)
let end: string; //A date formatted YYYY-MM-DD, to get info on how much the user has spent. You must submit both start and end.  (optional) (default to undefined)

const { status, data } = await apiInstance.listBudget(
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
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|
| **start** | [**string**] | A date formatted YYYY-MM-DD, to get info on how much the user has spent. You must submit both start and end.  | (optional) defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD, to get info on how much the user has spent. You must submit both start and end.  | (optional) defaults to undefined|


### Return type

**BudgetArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of budgets. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listBudgetLimit**
> BudgetLimitArray listBudgetLimit()

Get all budget limits for for this date range. 

### Example

```typescript
import {
    BudgetsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BudgetsApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.listBudgetLimit(
    start,
    end,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


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

# **listBudgetLimitByBudget**
> BudgetLimitArray listBudgetLimitByBudget()

Get all budget limits for this budget and the money spent, and money left. You can limit the list by submitting a date range as well. The \"spent\" array for each budget limit is NOT influenced by the start and end date of your query, but by the start and end date of the budget limit itself. 

### Example

```typescript
import {
    BudgetsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BudgetsApi(configuration);

let id: string; //The ID of the requested budget. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let start: string; //A date formatted YYYY-MM-DD.  (optional) (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (optional) (default to undefined)

const { status, data } = await apiInstance.listBudgetLimitByBudget(
    id,
    xTraceId,
    start,
    end
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the requested budget. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | (optional) defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | (optional) defaults to undefined|


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
|**200** | A list of budget limits applicable to this budget. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listTransactionByBudget**
> TransactionArray listTransactionByBudget()

Get all transactions linked to a budget, possibly limited by start and end

### Example

```typescript
import {
    BudgetsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BudgetsApi(configuration);

let id: string; //The ID of the budget. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)
let start: string; //A date formatted YYYY-MM-DD.  (optional) (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (optional) (default to undefined)
let type: TransactionTypeFilter; //Optional filter on the transaction type(s) returned (optional) (default to undefined)

const { status, data } = await apiInstance.listTransactionByBudget(
    id,
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
| **id** | [**string**] | The ID of the budget. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | (optional) defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | (optional) defaults to undefined|
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

# **listTransactionByBudgetLimit**
> TransactionArray listTransactionByBudgetLimit()

List all the transactions within one budget limit. The start and end date are dictated by the budget limit.

### Example

```typescript
import {
    BudgetsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BudgetsApi(configuration);

let id: string; //The ID of the budget. The budget limit MUST be associated to the budget ID. (default to undefined)
let limitId: string; //The ID of the budget limit. The budget limit MUST be associated to the budget ID. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)
let type: TransactionTypeFilter; //Optional filter on the transaction type(s) returned (optional) (default to undefined)

const { status, data } = await apiInstance.listTransactionByBudgetLimit(
    id,
    limitId,
    xTraceId,
    limit,
    page,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the budget. The budget limit MUST be associated to the budget ID. | defaults to undefined|
| **limitId** | [**string**] | The ID of the budget limit. The budget limit MUST be associated to the budget ID. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|
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

# **listTransactionWithoutBudget**
> TransactionArray listTransactionWithoutBudget()

Get all transactions NOT linked to a budget, possibly limited by start and end

### Example

```typescript
import {
    BudgetsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BudgetsApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)
let start: string; //A date formatted YYYY-MM-DD.  (optional) (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (optional) (default to undefined)

const { status, data } = await apiInstance.listTransactionWithoutBudget(
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
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | (optional) defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | (optional) defaults to undefined|


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
|**422** | Validation error. The body will have the exact details. |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **storeBudget**
> BudgetSingle storeBudget(budgetStore)

Creates a new budget. The data required can be submitted as a JSON body or as a list of parameters.

### Example

```typescript
import {
    BudgetsApi,
    Configuration,
    BudgetStore
} from './api';

const configuration = new Configuration();
const apiInstance = new BudgetsApi(configuration);

let budgetStore: BudgetStore; //JSON array or key=value pairs with the necessary budget information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.storeBudget(
    budgetStore,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **budgetStore** | **BudgetStore**| JSON array or key&#x3D;value pairs with the necessary budget information. See the model for the exact specifications. | |
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**BudgetSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | New budget stored, result in response. |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **storeBudgetLimit**
> BudgetLimitSingle storeBudgetLimit(budgetLimitStore)

Store a new budget limit under this budget.

### Example

```typescript
import {
    BudgetsApi,
    Configuration,
    BudgetLimitStore
} from './api';

const configuration = new Configuration();
const apiInstance = new BudgetsApi(configuration);

let id: string; //The ID of the budget. (default to undefined)
let budgetLimitStore: BudgetLimitStore; //JSON array or key=value pairs with the necessary budget information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.storeBudgetLimit(
    id,
    budgetLimitStore,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **budgetLimitStore** | **BudgetLimitStore**| JSON array or key&#x3D;value pairs with the necessary budget information. See the model for the exact specifications. | |
| **id** | [**string**] | The ID of the budget. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**BudgetLimitSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | New budget limit stored, result in response. |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateBudget**
> BudgetSingle updateBudget(budgetUpdate)

Update existing budget. This endpoint cannot be used to set budget amount limits.

### Example

```typescript
import {
    BudgetsApi,
    Configuration,
    BudgetUpdate
} from './api';

const configuration = new Configuration();
const apiInstance = new BudgetsApi(configuration);

let id: string; //The ID of the budget. (default to undefined)
let budgetUpdate: BudgetUpdate; //JSON array with updated budget information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.updateBudget(
    id,
    budgetUpdate,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **budgetUpdate** | **BudgetUpdate**| JSON array with updated budget information. See the model for the exact specifications. | |
| **id** | [**string**] | The ID of the budget. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**BudgetSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Updated budget stored, result in response |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateBudgetLimit**
> BudgetLimitSingle updateBudgetLimit(budgetLimit)

Update existing budget limit.

### Example

```typescript
import {
    BudgetsApi,
    Configuration,
    BudgetLimit
} from './api';

const configuration = new Configuration();
const apiInstance = new BudgetsApi(configuration);

let id: string; //The ID of the budget. The budget limit MUST be associated to the budget ID. (default to undefined)
let limitId: string; //The ID of the budget limit. The budget limit MUST be associated to the budget ID. (default to undefined)
let budgetLimit: BudgetLimit; //JSON array with updated budget limit information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.updateBudgetLimit(
    id,
    limitId,
    budgetLimit,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **budgetLimit** | **BudgetLimit**| JSON array with updated budget limit information. See the model for the exact specifications. | |
| **id** | [**string**] | The ID of the budget. The budget limit MUST be associated to the budget ID. | defaults to undefined|
| **limitId** | [**string**] | The ID of the budget limit. The budget limit MUST be associated to the budget ID. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**BudgetLimitSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Updated budget limit stored, result in response |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

