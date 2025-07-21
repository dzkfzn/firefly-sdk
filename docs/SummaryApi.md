# SummaryApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getBasicSummary**](#getbasicsummary) | **GET** /v1/summary/basic | Returns basic sums of the users data.|

# **getBasicSummary**
> { [key: string]: BasicSummaryEntry; } getBasicSummary()

Returns basic sums of the users data, like the net worth, spent and earned amounts. It is multi-currency, and is used in Firefly III to populate the dashboard. 

### Example

```typescript
import {
    SummaryApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new SummaryApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let currencyCode: string; //A currency code like EUR or USD, to filter the result.  (optional) (default to undefined)

const { status, data } = await apiInstance.getBasicSummary(
    start,
    end,
    xTraceId,
    currencyCode
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **currencyCode** | [**string**] | A currency code like EUR or USD, to filter the result.  | (optional) defaults to undefined|


### Return type

**{ [key: string]: BasicSummaryEntry; }**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | An array of sums. It depends on the user what you can expect to get back, so please try this out on the demo site. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

