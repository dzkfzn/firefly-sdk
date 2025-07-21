# InsightApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**insightExpenseAsset**](#insightexpenseasset) | **GET** /v1/insight/expense/asset | Insight into expenses, grouped by asset account.|
|[**insightExpenseBill**](#insightexpensebill) | **GET** /v1/insight/expense/bill | Insight into expenses, grouped by bill.|
|[**insightExpenseBudget**](#insightexpensebudget) | **GET** /v1/insight/expense/budget | Insight into expenses, grouped by budget.|
|[**insightExpenseCategory**](#insightexpensecategory) | **GET** /v1/insight/expense/category | Insight into expenses, grouped by category.|
|[**insightExpenseExpense**](#insightexpenseexpense) | **GET** /v1/insight/expense/expense | Insight into expenses, grouped by expense account.|
|[**insightExpenseNoBill**](#insightexpensenobill) | **GET** /v1/insight/expense/no-bill | Insight into expenses, without bill.|
|[**insightExpenseNoBudget**](#insightexpensenobudget) | **GET** /v1/insight/expense/no-budget | Insight into expenses, without budget.|
|[**insightExpenseNoCategory**](#insightexpensenocategory) | **GET** /v1/insight/expense/no-category | Insight into expenses, without category.|
|[**insightExpenseNoTag**](#insightexpensenotag) | **GET** /v1/insight/expense/no-tag | Insight into expenses, without tag.|
|[**insightExpenseTag**](#insightexpensetag) | **GET** /v1/insight/expense/tag | Insight into expenses, grouped by tag.|
|[**insightExpenseTotal**](#insightexpensetotal) | **GET** /v1/insight/expense/total | Insight into total expenses.|
|[**insightIncomeAsset**](#insightincomeasset) | **GET** /v1/insight/income/asset | Insight into income, grouped by asset account.|
|[**insightIncomeCategory**](#insightincomecategory) | **GET** /v1/insight/income/category | Insight into income, grouped by category.|
|[**insightIncomeNoCategory**](#insightincomenocategory) | **GET** /v1/insight/income/no-category | Insight into income, without category.|
|[**insightIncomeNoTag**](#insightincomenotag) | **GET** /v1/insight/income/no-tag | Insight into income, without tag.|
|[**insightIncomeRevenue**](#insightincomerevenue) | **GET** /v1/insight/income/revenue | Insight into income, grouped by revenue account.|
|[**insightIncomeTag**](#insightincometag) | **GET** /v1/insight/income/tag | Insight into income, grouped by tag.|
|[**insightIncomeTotal**](#insightincometotal) | **GET** /v1/insight/income/total | Insight into total income.|
|[**insightTransferCategory**](#insighttransfercategory) | **GET** /v1/insight/transfer/category | Insight into transfers, grouped by category.|
|[**insightTransferNoCategory**](#insighttransfernocategory) | **GET** /v1/insight/transfer/no-category | Insight into transfers, without category.|
|[**insightTransferNoTag**](#insighttransfernotag) | **GET** /v1/insight/transfer/no-tag | Insight into expenses, without tag.|
|[**insightTransferTag**](#insighttransfertag) | **GET** /v1/insight/transfer/tag | Insight into transfers, grouped by tag.|
|[**insightTransferTotal**](#insighttransfertotal) | **GET** /v1/insight/transfer/total | Insight into total transfers.|
|[**insightTransfers**](#insighttransfers) | **GET** /v1/insight/transfer/asset | Insight into transfers, grouped by account.|

# **insightExpenseAsset**
> Array<InsightGroupEntry> insightExpenseAsset()

This endpoint gives a summary of the expenses made by the user, grouped by asset account. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightExpenseAsset(
    start,
    end,
    xTraceId,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightGroupEntry>**

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
|**200** | A list of asset accounts and expense details. Each asset account has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightExpenseBill**
> Array<InsightGroupEntry> insightExpenseBill()

This endpoint gives a summary of the expenses made by the user, grouped by (any) bill. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let bills: Array<number>; //The bills to be included in the results.  (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightExpenseBill(
    start,
    end,
    xTraceId,
    bills,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **bills** | **Array&lt;number&gt;** | The bills to be included in the results.  | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightGroupEntry>**

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
|**200** | A list of budget and expense details. Each budget has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightExpenseBudget**
> Array<InsightGroupEntry> insightExpenseBudget()

This endpoint gives a summary of the expenses made by the user, grouped by (any) budget. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let budgets: Array<number>; //The budgets to be included in the results.  (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightExpenseBudget(
    start,
    end,
    xTraceId,
    budgets,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **budgets** | **Array&lt;number&gt;** | The budgets to be included in the results.  | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightGroupEntry>**

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
|**200** | A list of budget and expense details. Each budget has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightExpenseCategory**
> Array<InsightGroupEntry> insightExpenseCategory()

This endpoint gives a summary of the expenses made by the user, grouped by (any) category. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let categories: Array<number>; //The categories to be included in the results.  (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightExpenseCategory(
    start,
    end,
    xTraceId,
    categories,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **categories** | **Array&lt;number&gt;** | The categories to be included in the results.  | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightGroupEntry>**

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
|**200** | A list of category and expense details. Each category has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightExpenseExpense**
> Array<InsightGroupEntry> insightExpenseExpense()

This endpoint gives a summary of the expenses made by the user, grouped by expense account. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you add the accounts ID\'s of expense accounts, only those accounts are included in the results. If you include ID\'s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. You can combine both asset / liability and expense account ID\'s. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightExpenseExpense(
    start,
    end,
    xTraceId,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you add the accounts ID\&#39;s of expense accounts, only those accounts are included in the results. If you include ID\&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. You can combine both asset / liability and expense account ID\&#39;s. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightGroupEntry>**

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
|**200** | A list of expense accounts and expense details. Each expense acccount has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightExpenseNoBill**
> Array<InsightTotalEntry> insightExpenseNoBill()

This endpoint gives a summary of the expenses made by the user, including only expenses with no bill. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightExpenseNoBill(
    start,
    end,
    xTraceId,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightTotalEntry>**

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
|**200** | A list of expense details. One row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightExpenseNoBudget**
> Array<InsightTotalEntry> insightExpenseNoBudget()

This endpoint gives a summary of the expenses made by the user, including only expenses with no budget. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightExpenseNoBudget(
    start,
    end,
    xTraceId,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightTotalEntry>**

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
|**200** | A list of expense details. One row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightExpenseNoCategory**
> Array<InsightTotalEntry> insightExpenseNoCategory()

This endpoint gives a summary of the expenses made by the user, including only expenses with no category. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightExpenseNoCategory(
    start,
    end,
    xTraceId,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightTotalEntry>**

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
|**200** | A list of expense details. One row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightExpenseNoTag**
> Array<InsightTotalEntry> insightExpenseNoTag()

This endpoint gives a summary of the expenses made by the user, including only expenses with no tag. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightExpenseNoTag(
    start,
    end,
    xTraceId,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightTotalEntry>**

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
|**200** | A list of expense details. One row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightExpenseTag**
> Array<InsightGroupEntry> insightExpenseTag()

This endpoint gives a summary of the expenses made by the user, grouped by (any) tag. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let tags: Array<number>; //The tags to be included in the results.  (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightExpenseTag(
    start,
    end,
    xTraceId,
    tags,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **tags** | **Array&lt;number&gt;** | The tags to be included in the results.  | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightGroupEntry>**

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
|**200** | A list of tag and expense details. Each tag has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightExpenseTotal**
> Array<InsightTotalEntry> insightExpenseTotal()

This endpoint gives a sum of the total expenses made by the user. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightExpenseTotal(
    start,
    end,
    xTraceId,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightTotalEntry>**

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
|**200** | A list of sums in different currencies. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightIncomeAsset**
> Array<InsightGroupEntry> insightIncomeAsset()

This endpoint gives a summary of the income received by the user, grouped by asset account. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightIncomeAsset(
    start,
    end,
    xTraceId,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightGroupEntry>**

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
|**200** | A list of asset accounts and income details. Each asset account has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightIncomeCategory**
> Array<InsightGroupEntry> insightIncomeCategory()

This endpoint gives a summary of the income received by the user, grouped by (any) category. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let categories: Array<number>; //The categories to be included in the results.  (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightIncomeCategory(
    start,
    end,
    xTraceId,
    categories,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **categories** | **Array&lt;number&gt;** | The categories to be included in the results.  | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightGroupEntry>**

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
|**200** | A list of category and income details. Each category has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightIncomeNoCategory**
> Array<InsightTotalEntry> insightIncomeNoCategory()

This endpoint gives a summary of the income received by the user, including only income with no category. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightIncomeNoCategory(
    start,
    end,
    xTraceId,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightTotalEntry>**

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
|**200** | A list of income details. One row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightIncomeNoTag**
> Array<InsightTotalEntry> insightIncomeNoTag()

This endpoint gives a summary of the income received by the user, including only income with no tag. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightIncomeNoTag(
    start,
    end,
    xTraceId,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightTotalEntry>**

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
|**200** | A list of income details. One row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightIncomeRevenue**
> Array<InsightGroupEntry> insightIncomeRevenue()

This endpoint gives a summary of the income received by the user, grouped by revenue account. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you add the accounts ID\'s of revenue accounts, only those accounts are included in the results. If you include ID\'s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. You can combine both asset / liability and deposit account ID\'s. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightIncomeRevenue(
    start,
    end,
    xTraceId,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you add the accounts ID\&#39;s of revenue accounts, only those accounts are included in the results. If you include ID\&#39;s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. You can combine both asset / liability and deposit account ID\&#39;s. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightGroupEntry>**

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
|**200** | A list of revenue accounts and income details. Each revenue acccount has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightIncomeTag**
> Array<InsightGroupEntry> insightIncomeTag()

This endpoint gives a summary of the income received by the user, grouped by (any) tag. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let tags: Array<number>; //The tags to be included in the results.  (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightIncomeTag(
    start,
    end,
    xTraceId,
    tags,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **tags** | **Array&lt;number&gt;** | The tags to be included in the results.  | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightGroupEntry>**

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
|**200** | A list of tag and income details. Each tag has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightIncomeTotal**
> Array<InsightTotalEntry> insightIncomeTotal()

This endpoint gives a sum of the total income received by the user. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightIncomeTotal(
    start,
    end,
    xTraceId,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightTotalEntry>**

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
|**200** | A list of sums in different currencies. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightTransferCategory**
> Array<InsightGroupEntry> insightTransferCategory()

This endpoint gives a summary of the transfers made by the user, grouped by (any) category. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let categories: Array<number>; //The categories to be included in the results.  (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only transfers between those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightTransferCategory(
    start,
    end,
    xTraceId,
    categories,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **categories** | **Array&lt;number&gt;** | The categories to be included in the results.  | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only transfers between those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightGroupEntry>**

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
|**200** | A list of category and transfer details. Each category has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightTransferNoCategory**
> Array<InsightTotalEntry> insightTransferNoCategory()

This endpoint gives a summary of the transfers made by the user, including only transfers with no category. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only transfers between those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightTransferNoCategory(
    start,
    end,
    xTraceId,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only transfers between those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightTotalEntry>**

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
|**200** | A list of transfer details. One row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightTransferNoTag**
> Array<InsightTotalEntry> insightTransferNoTag()

This endpoint gives a summary of the transfers made by the user, including only transfers with no tag. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only transfers from those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightTransferNoTag(
    start,
    end,
    xTraceId,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only transfers from those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightTotalEntry>**

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
|**200** | A list of transfer details. One row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightTransferTag**
> Array<InsightGroupEntry> insightTransferTag()

This endpoint gives a summary of the transfers created by the user, grouped by (any) tag. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let tags: Array<number>; //The tags to be included in the results.  (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only transfers between those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightTransferTag(
    start,
    end,
    xTraceId,
    tags,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **tags** | **Array&lt;number&gt;** | The tags to be included in the results.  | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only transfers between those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightGroupEntry>**

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
|**200** | A list of tag and transfer details. Each tag has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightTransferTotal**
> Array<InsightTotalEntry> insightTransferTotal()

This endpoint gives a sum of the total amount transfers made by the user. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only transfers between those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightTransferTotal(
    start,
    end,
    xTraceId,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only transfers between those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightTotalEntry>**

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
|**200** | A list of sums in different currencies. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **insightTransfers**
> Array<InsightTransferEntry> insightTransfers()

This endpoint gives a summary of the transfers made by the user, grouped by asset account or lability. 

### Example

```typescript
import {
    InsightApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new InsightApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: Array<number>; //The accounts to be included in the results. If you include ID\'s of asset accounts or liabilities, only transfers between those asset accounts / liabilities will be included. Other account ID\'s will be ignored.  (optional) (default to undefined)

const { status, data } = await apiInstance.insightTransfers(
    start,
    end,
    xTraceId,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | The accounts to be included in the results. If you include ID\&#39;s of asset accounts or liabilities, only transfers between those asset accounts / liabilities will be included. Other account ID\&#39;s will be ignored.  | (optional) defaults to undefined|


### Return type

**Array<InsightTransferEntry>**

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
|**200** | A list of asset accounts and transfer details. Each asset account has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

