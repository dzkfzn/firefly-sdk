# RecurrencesApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteRecurrence**](#deleterecurrence) | **DELETE** /v1/recurrences/{id} | Delete a recurring transaction.|
|[**getRecurrence**](#getrecurrence) | **GET** /v1/recurrences/{id} | Get a single recurring transaction.|
|[**listRecurrence**](#listrecurrence) | **GET** /v1/recurrences | List all recurring transactions.|
|[**listTransactionByRecurrence**](#listtransactionbyrecurrence) | **GET** /v1/recurrences/{id}/transactions | List all transactions created by a recurring transaction.|
|[**storeRecurrence**](#storerecurrence) | **POST** /v1/recurrences | Store a new recurring transaction|
|[**updateRecurrence**](#updaterecurrence) | **PUT** /v1/recurrences/{id} | Update existing recurring transaction.|

# **deleteRecurrence**
> deleteRecurrence()

Delete a recurring transaction. Transactions created by the recurring transaction will not be deleted.

### Example

```typescript
import {
    RecurrencesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new RecurrencesApi(configuration);

let id: string; //The ID of the recurring transaction. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.deleteRecurrence(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the recurring transaction. | defaults to undefined|
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
|**204** | Recurring transaction deleted. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getRecurrence**
> RecurrenceSingle getRecurrence()

Get a single recurring transaction.

### Example

```typescript
import {
    RecurrencesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new RecurrencesApi(configuration);

let id: string; //The ID of the recurring transaction. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getRecurrence(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the recurring transaction. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**RecurrenceSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The requested recurring transaction |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listRecurrence**
> RecurrenceArray listRecurrence()

List all recurring transactions.

### Example

```typescript
import {
    RecurrencesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new RecurrencesApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listRecurrence(
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

**RecurrenceArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of recurring transactions. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listTransactionByRecurrence**
> TransactionArray listTransactionByRecurrence()

List all transactions created by a recurring transaction, optionally limited to the date ranges specified.

### Example

```typescript
import {
    RecurrencesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new RecurrencesApi(configuration);

let id: string; //The ID of the recurring transaction. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)
let start: string; //A date formatted YYYY-MM-DD. Both the start and end date must be present.  (optional) (default to undefined)
let end: string; //A date formatted YYYY-MM-DD. Both the start and end date must be present.  (optional) (default to undefined)
let type: TransactionTypeFilter; //Optional filter on the transaction type(s) returned (optional) (default to undefined)

const { status, data } = await apiInstance.listTransactionByRecurrence(
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
| **id** | [**string**] | The ID of the recurring transaction. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|
| **start** | [**string**] | A date formatted YYYY-MM-DD. Both the start and end date must be present.  | (optional) defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD. Both the start and end date must be present.  | (optional) defaults to undefined|
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
|**200** | A list of transactions |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **storeRecurrence**
> RecurrenceSingle storeRecurrence(recurrenceStore)

Creates a new recurring transaction. The data required can be submitted as a JSON body or as a list of parameters.

### Example

```typescript
import {
    RecurrencesApi,
    Configuration,
    RecurrenceStore
} from './api';

const configuration = new Configuration();
const apiInstance = new RecurrencesApi(configuration);

let recurrenceStore: RecurrenceStore; //JSON array or key=value pairs with the necessary recurring transaction information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.storeRecurrence(
    recurrenceStore,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **recurrenceStore** | **RecurrenceStore**| JSON array or key&#x3D;value pairs with the necessary recurring transaction information. See the model for the exact specifications. | |
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**RecurrenceSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | New recurring transaction stored, result in response. |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateRecurrence**
> RecurrenceSingle updateRecurrence(recurrenceUpdate)

Update existing recurring transaction.

### Example

```typescript
import {
    RecurrencesApi,
    Configuration,
    RecurrenceUpdate
} from './api';

const configuration = new Configuration();
const apiInstance = new RecurrencesApi(configuration);

let id: string; //The ID of the recurring transaction. (default to undefined)
let recurrenceUpdate: RecurrenceUpdate; //JSON array with updated recurring transaction information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.updateRecurrence(
    id,
    recurrenceUpdate,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **recurrenceUpdate** | **RecurrenceUpdate**| JSON array with updated recurring transaction information. See the model for the exact specifications. | |
| **id** | [**string**] | The ID of the recurring transaction. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**RecurrenceSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Updated recurring transaction stored, result in response |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

