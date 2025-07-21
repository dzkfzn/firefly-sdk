# PiggyBanksApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deletePiggyBank**](#deletepiggybank) | **DELETE** /v1/piggy-banks/{id} | Delete a piggy bank.|
|[**getPiggyBank**](#getpiggybank) | **GET** /v1/piggy-banks/{id} | Get a single piggy bank.|
|[**listAttachmentByPiggyBank**](#listattachmentbypiggybank) | **GET** /v1/piggy-banks/{id}/attachments | Lists all attachments.|
|[**listEventByPiggyBank**](#listeventbypiggybank) | **GET** /v1/piggy-banks/{id}/events | List all events linked to a piggy bank.|
|[**listPiggyBank**](#listpiggybank) | **GET** /v1/piggy-banks | List all piggy banks.|
|[**storePiggyBank**](#storepiggybank) | **POST** /v1/piggy-banks | Store a new piggy bank|
|[**updatePiggyBank**](#updatepiggybank) | **PUT** /v1/piggy-banks/{id} | Update existing piggy bank.|

# **deletePiggyBank**
> deletePiggyBank()

Delete a piggy bank.

### Example

```typescript
import {
    PiggyBanksApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new PiggyBanksApi(configuration);

let id: string; //The ID of the piggy bank. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.deletePiggyBank(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the piggy bank. | defaults to undefined|
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
|**204** | Piggy bank deleted. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPiggyBank**
> PiggyBankSingle getPiggyBank()

Get a single piggy bank.

### Example

```typescript
import {
    PiggyBanksApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new PiggyBanksApi(configuration);

let id: string; //The ID of the piggy bank. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getPiggyBank(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the piggy bank. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**PiggyBankSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The requested piggy bank |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listAttachmentByPiggyBank**
> AttachmentArray listAttachmentByPiggyBank()

Lists all attachments.

### Example

```typescript
import {
    PiggyBanksApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new PiggyBanksApi(configuration);

let id: string; //The ID of the piggy bank. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listAttachmentByPiggyBank(
    id,
    xTraceId,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the piggy bank. | defaults to undefined|
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
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listEventByPiggyBank**
> PiggyBankEventArray listEventByPiggyBank()

List all events linked to a piggy bank (adding and removing money).

### Example

```typescript
import {
    PiggyBanksApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new PiggyBanksApi(configuration);

let id: string; //The ID of the piggy bank (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listEventByPiggyBank(
    id,
    xTraceId,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the piggy bank | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|


### Return type

**PiggyBankEventArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of piggy bank related events |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listPiggyBank**
> PiggyBankArray listPiggyBank()

List all piggy banks.

### Example

```typescript
import {
    PiggyBanksApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new PiggyBanksApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listPiggyBank(
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

**PiggyBankArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of piggy banks |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **storePiggyBank**
> PiggyBankSingle storePiggyBank(piggyBankStore)

Creates a new piggy bank. The data required can be submitted as a JSON body or as a list of parameters.

### Example

```typescript
import {
    PiggyBanksApi,
    Configuration,
    PiggyBankStore
} from './api';

const configuration = new Configuration();
const apiInstance = new PiggyBanksApi(configuration);

let piggyBankStore: PiggyBankStore; //JSON array or key=value pairs with the necessary piggy bank information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.storePiggyBank(
    piggyBankStore,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **piggyBankStore** | **PiggyBankStore**| JSON array or key&#x3D;value pairs with the necessary piggy bank information. See the model for the exact specifications. | |
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**PiggyBankSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | New piggy bank stored, result in response. |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updatePiggyBank**
> PiggyBankSingle updatePiggyBank(piggyBankUpdate)

Update existing piggy bank.

### Example

```typescript
import {
    PiggyBanksApi,
    Configuration,
    PiggyBankUpdate
} from './api';

const configuration = new Configuration();
const apiInstance = new PiggyBanksApi(configuration);

let id: string; //The ID of the piggy bank (default to undefined)
let piggyBankUpdate: PiggyBankUpdate; //JSON array with updated piggy bank information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.updatePiggyBank(
    id,
    piggyBankUpdate,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **piggyBankUpdate** | **PiggyBankUpdate**| JSON array with updated piggy bank information. See the model for the exact specifications. | |
| **id** | [**string**] | The ID of the piggy bank | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**PiggyBankSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Updated piggy bank stored, result in response |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

