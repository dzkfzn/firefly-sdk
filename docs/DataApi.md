# DataApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**bulkUpdateTransactions**](#bulkupdatetransactions) | **POST** /v1/data/bulk/transactions | Bulk update transaction properties. For more information, see https://docs.firefly-iii.org/references/firefly-iii/api/specials/|
|[**destroyData**](#destroydata) | **DELETE** /v1/data/destroy | Endpoint to destroy user data|
|[**exportAccounts**](#exportaccounts) | **GET** /v1/data/export/accounts | Export account data from Firefly III|
|[**exportBills**](#exportbills) | **GET** /v1/data/export/bills | Export bills from Firefly III|
|[**exportBudgets**](#exportbudgets) | **GET** /v1/data/export/budgets | Export budgets and budget amount data from Firefly III|
|[**exportCategories**](#exportcategories) | **GET** /v1/data/export/categories | Export category data from Firefly III|
|[**exportPiggies**](#exportpiggies) | **GET** /v1/data/export/piggy-banks | Export piggy banks from Firefly III|
|[**exportRecurring**](#exportrecurring) | **GET** /v1/data/export/recurring | Export recurring transaction data from Firefly III|
|[**exportRules**](#exportrules) | **GET** /v1/data/export/rules | Export rule groups and rule data from Firefly III|
|[**exportTags**](#exporttags) | **GET** /v1/data/export/tags | Export tag data from Firefly III|
|[**exportTransactions**](#exporttransactions) | **GET** /v1/data/export/transactions | Export transaction data from Firefly III|
|[**purgeData**](#purgedata) | **DELETE** /v1/data/purge | Endpoint to purge user data|

# **bulkUpdateTransactions**
> bulkUpdateTransactions()

Allows you to update transactions in bulk. 

### Example

```typescript
import {
    DataApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DataApi(configuration);

let query: string; //The JSON query. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.bulkUpdateTransactions(
    query,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **query** | [**string**] | The JSON query. | defaults to undefined|
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
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**204** | Empty response when the update was successful. A future improvement is to include the changed transactions. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **destroyData**
> destroyData()

A call to this endpoint deletes the requested data type. Use it with care and always with user permission. The demo user is incapable of using this endpoint. 

### Example

```typescript
import {
    DataApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DataApi(configuration);

let objects: DataDestroyObject; //The type of data that you wish to destroy. You can only use one at a time. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.destroyData(
    objects,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **objects** | **DataDestroyObject** | The type of data that you wish to destroy. You can only use one at a time. | defaults to undefined|
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
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**204** | Empty response when data has been destroyed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exportAccounts**
> File exportAccounts()

This endpoint allows you to export your accounts from Firefly III into a file. Currently supports CSV exports only. 

### Example

```typescript
import {
    DataApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DataApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let type: ExportFileFilter; //The file type the export file (CSV is currently the only option). (optional) (default to undefined)

const { status, data } = await apiInstance.exportAccounts(
    xTraceId,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | (optional) defaults to undefined|


### Return type

**File**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exportBills**
> File exportBills()

This endpoint allows you to export your bills from Firefly III into a file. Currently supports CSV exports only. 

### Example

```typescript
import {
    DataApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DataApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let type: ExportFileFilter; //The file type the export file (CSV is currently the only option). (optional) (default to undefined)

const { status, data } = await apiInstance.exportBills(
    xTraceId,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | (optional) defaults to undefined|


### Return type

**File**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exportBudgets**
> File exportBudgets()

This endpoint allows you to export your budgets and associated budget data from Firefly III into a file. Currently supports CSV exports only. 

### Example

```typescript
import {
    DataApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DataApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let type: ExportFileFilter; //The file type the export file (CSV is currently the only option). (optional) (default to undefined)

const { status, data } = await apiInstance.exportBudgets(
    xTraceId,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | (optional) defaults to undefined|


### Return type

**File**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exportCategories**
> File exportCategories()

This endpoint allows you to export your categories from Firefly III into a file. Currently supports CSV exports only. 

### Example

```typescript
import {
    DataApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DataApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let type: ExportFileFilter; //The file type the export file (CSV is currently the only option). (optional) (default to undefined)

const { status, data } = await apiInstance.exportCategories(
    xTraceId,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | (optional) defaults to undefined|


### Return type

**File**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exportPiggies**
> File exportPiggies()

This endpoint allows you to export your piggy banks from Firefly III into a file. Currently supports CSV exports only. 

### Example

```typescript
import {
    DataApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DataApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let type: ExportFileFilter; //The file type the export file (CSV is currently the only option). (optional) (default to undefined)

const { status, data } = await apiInstance.exportPiggies(
    xTraceId,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | (optional) defaults to undefined|


### Return type

**File**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exportRecurring**
> File exportRecurring()

This endpoint allows you to export your recurring transactions from Firefly III into a file. Currently supports CSV exports only. 

### Example

```typescript
import {
    DataApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DataApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let type: ExportFileFilter; //The file type the export file (CSV is currently the only option). (optional) (default to undefined)

const { status, data } = await apiInstance.exportRecurring(
    xTraceId,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | (optional) defaults to undefined|


### Return type

**File**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exportRules**
> File exportRules()

This endpoint allows you to export your rules and rule groups from Firefly III into a file. Currently supports CSV exports only. 

### Example

```typescript
import {
    DataApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DataApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let type: ExportFileFilter; //The file type the export file (CSV is currently the only option). (optional) (default to undefined)

const { status, data } = await apiInstance.exportRules(
    xTraceId,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | (optional) defaults to undefined|


### Return type

**File**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exportTags**
> File exportTags()

This endpoint allows you to export your tags from Firefly III into a file. Currently supports CSV exports only. 

### Example

```typescript
import {
    DataApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DataApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let type: ExportFileFilter; //The file type the export file (CSV is currently the only option). (optional) (default to undefined)

const { status, data } = await apiInstance.exportTags(
    xTraceId,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | (optional) defaults to undefined|


### Return type

**File**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exportTransactions**
> File exportTransactions()

This endpoint allows you to export transactions from Firefly III into a file. Currently supports CSV exports only. 

### Example

```typescript
import {
    DataApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DataApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let accounts: string; //Limit the export of transactions to these accounts only. Only asset accounts will be accepted. Other types will be silently dropped.  (optional) (default to undefined)
let type: ExportFileFilter; //The file type the export file (CSV is currently the only option). (optional) (default to undefined)

const { status, data } = await apiInstance.exportTransactions(
    start,
    end,
    xTraceId,
    accounts,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **accounts** | [**string**] | Limit the export of transactions to these accounts only. Only asset accounts will be accepted. Other types will be silently dropped.  | (optional) defaults to undefined|
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | (optional) defaults to undefined|


### Return type

**File**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **purgeData**
> purgeData()

A call to this endpoint purges all previously deleted data. Use it with care and always with user permission. The demo user is incapable of using this endpoint. 

### Example

```typescript
import {
    DataApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DataApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.purgeData(
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
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
|**401** | Unauthenticated |  -  |
|**400** | Bad request |  -  |
|**404** | Page not found |  -  |
|**500** | Internal exception |  -  |
|**204** | Empty response when data has been purged. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

