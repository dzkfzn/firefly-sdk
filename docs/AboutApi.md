# AboutApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getAbout**](#getabout) | **GET** /v1/about | System information end point.|
|[**getCron**](#getcron) | **GET** /v1/cron/{cliToken} | Cron job endpoint|
|[**getCurrentUser**](#getcurrentuser) | **GET** /v1/about/user | Currently authenticated user endpoint.|

# **getAbout**
> SystemInfo getAbout()

Returns general system information and versions of the (supporting) software. 

### Example

```typescript
import {
    AboutApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AboutApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getAbout(
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**SystemInfo**

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
|**200** | The available system information |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getCron**
> CronResult getCron()

Firefly III has one endpoint for its various cron related tasks. Send a GET to this endpoint to run the cron. The cron requires the CLI token to be present. The cron job will fire for all users. 

### Example

```typescript
import {
    AboutApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AboutApi(configuration);

let cliToken: string; //The CLI token of any user in Firefly III, required to run the cron job. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let date: string; //A date formatted YYYY-MM-DD. This can be used to make the cron job pretend it\'s running on another day.  (optional) (default to undefined)
let force: boolean; //Forces the cron job to fire, regardless of whether it has fired before. This may result in double transactions or weird budgets, so be careful.  (optional) (default to undefined)

const { status, data } = await apiInstance.getCron(
    cliToken,
    xTraceId,
    date,
    force
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **cliToken** | [**string**] | The CLI token of any user in Firefly III, required to run the cron job. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **date** | [**string**] | A date formatted YYYY-MM-DD. This can be used to make the cron job pretend it\&#39;s running on another day.  | (optional) defaults to undefined|
| **force** | [**boolean**] | Forces the cron job to fire, regardless of whether it has fired before. This may result in double transactions or weird budgets, so be careful.  | (optional) defaults to undefined|


### Return type

**CronResult**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The result of the cron job(s) firing. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getCurrentUser**
> UserSingle getCurrentUser()

Returns the currently authenticated user. 

### Example

```typescript
import {
    AboutApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AboutApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getCurrentUser(
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**UserSingle**

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
|**200** | The user |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

