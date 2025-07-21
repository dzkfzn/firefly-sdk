# AvailableBudgetsApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getAvailableBudget**](#getavailablebudget) | **GET** /v1/available-budgets/{id} | Get a single available budget.|
|[**listAvailableBudget**](#listavailablebudget) | **GET** /v1/available-budgets | List all available budget amounts.|

# **getAvailableBudget**
> AvailableBudgetSingle getAvailableBudget()

Get a single available budget, by ID.

### Example

```typescript
import {
    AvailableBudgetsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AvailableBudgetsApi(configuration);

let id: string; //The ID of the available budget. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getAvailableBudget(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the available budget. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**AvailableBudgetSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/vnd.api+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | The requested available budget |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listAvailableBudget**
> AvailableBudgetArray listAvailableBudget()

Firefly III allows users to set the amount that is available to be budgeted in so-called \"available budgets\". For example, the user could have 1200,- available to be divided during the coming month. This amount is used on the /budgets page. This endpoint returns all of these amounts and the periods for which they are set. 

### Example

```typescript
import {
    AvailableBudgetsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AvailableBudgetsApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)
let start: string; //A date formatted YYYY-MM-DD.  (optional) (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (optional) (default to undefined)

const { status, data } = await apiInstance.listAvailableBudget(
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

**AvailableBudgetArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/vnd.api+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | A list of available budget amounts. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

