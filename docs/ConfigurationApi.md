# ConfigurationApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getConfiguration**](#getconfiguration) | **GET** /v1/configuration | Get Firefly III system configuration values.|
|[**getSingleConfiguration**](#getsingleconfiguration) | **GET** /v1/configuration/{name} | Get a single Firefly III system configuration value|
|[**setConfiguration**](#setconfiguration) | **PUT** /v1/configuration/{name} | Update configuration value|

# **getConfiguration**
> Array<Configuration> getConfiguration()

Returns all editable and not-editable configuration values for this Firefly III installation

### Example

```typescript
import {
    ConfigurationApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ConfigurationApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getConfiguration(
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**Array<Configuration>**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/x-www-form-urlencoded


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | System configuration values |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getSingleConfiguration**
> ConfigurationSingle getSingleConfiguration()

Returns one configuration variable for this Firefly III installation

### Example

```typescript
import {
    ConfigurationApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new ConfigurationApi(configuration);

let name: ConfigValueFilter; //The name of the configuration value you want to know. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getSingleConfiguration(
    name,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **name** | **ConfigValueFilter** | The name of the configuration value you want to know. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**ConfigurationSingle**

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
|**200** | One system configuration value |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **setConfiguration**
> ConfigurationSingle setConfiguration()

Set a single configuration value. Not all configuration values can be updated so the list of accepted configuration variables is small.

### Example

```typescript
import {
    ConfigurationApi,
    Configuration,
    PolymorphicProperty
} from './api';

const configuration = new Configuration();
const apiInstance = new ConfigurationApi(configuration);

let name: ConfigValueUpdateFilter; //The name of the configuration value you want to update. (default to undefined)
let value: PolymorphicProperty; // (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.setConfiguration(
    name,
    value,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **name** | **ConfigValueUpdateFilter** | The name of the configuration value you want to update. | defaults to undefined|
| **value** | **PolymorphicProperty** |  | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**ConfigurationSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded, application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | New configuration value stored, result in response. |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

