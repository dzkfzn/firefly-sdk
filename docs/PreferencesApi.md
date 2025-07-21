# PreferencesApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getPreference**](#getpreference) | **GET** /v1/preferences/{name} | Return a single preference.|
|[**listPreference**](#listpreference) | **GET** /v1/preferences | List all users preferences.|
|[**storePreference**](#storepreference) | **POST** /v1/preferences | Store a new preference for this user.|
|[**updatePreference**](#updatepreference) | **PUT** /v1/preferences/{name} | Update preference|

# **getPreference**
> PreferenceSingle getPreference()

Return a single preference and the value.

### Example

```typescript
import {
    PreferencesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new PreferencesApi(configuration);

let name: string; //The name of the preference. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getPreference(
    name,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **name** | [**string**] | The name of the preference. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**PreferenceSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A single preference. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listPreference**
> PreferenceArray listPreference()

List all of the preferences of the user.

### Example

```typescript
import {
    PreferencesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new PreferencesApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listPreference(
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

**PreferenceArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of preferences. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **storePreference**
> PreferenceSingle storePreference(preference)

This endpoint creates a new preference. The name and data are free-format, and entirely up to you. If the preference is not used in Firefly III itself it may not be configurable through the user interface, but you can use this endpoint to persist custom data for your own app.

### Example

```typescript
import {
    PreferencesApi,
    Configuration,
    Preference
} from './api';

const configuration = new Configuration();
const apiInstance = new PreferencesApi(configuration);

let preference: Preference; //JSON array with the necessary preference information or key=value pairs. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.storePreference(
    preference,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **preference** | **Preference**| JSON array with the necessary preference information or key&#x3D;value pairs. See the model for the exact specifications. | |
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**PreferenceSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | New account stored, result in response. |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updatePreference**
> PreferenceSingle updatePreference(preferenceUpdate)

Update a user\'s preference.

### Example

```typescript
import {
    PreferencesApi,
    Configuration,
    PreferenceUpdate
} from './api';

const configuration = new Configuration();
const apiInstance = new PreferencesApi(configuration);

let name: string; //The name of the preference. Will always overwrite. Will be created if it does not exist. (default to undefined)
let preferenceUpdate: PreferenceUpdate; //JSON array or key=value pairs with the necessary preference information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.updatePreference(
    name,
    preferenceUpdate,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **preferenceUpdate** | **PreferenceUpdate**| JSON array or key&#x3D;value pairs with the necessary preference information. See the model for the exact specifications. | |
| **name** | [**string**] | The name of the preference. Will always overwrite. Will be created if it does not exist. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**PreferenceSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Updated preference. |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

