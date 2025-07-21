# ChartsApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getChartAccountOverview**](#getchartaccountoverview) | **GET** /v1/chart/account/overview | Dashboard chart with asset account balance information.|

# **getChartAccountOverview**
> Array<ChartDataSet> getChartAccountOverview()

This endpoint returns the data required to generate a chart with basic asset account balance information. 

### Example

```typescript
import {
    ChartsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ChartsApi(configuration);

let start: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getChartAccountOverview(
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

**Array<ChartDataSet>**

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
|**200** | Line chart oriented chart information. Check out the model for more details. Each entry is a line (or bar) in the chart. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

