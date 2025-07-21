# AttachmentsApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteAttachment**](#deleteattachment) | **DELETE** /v1/attachments/{id} | Delete an attachment.|
|[**downloadAttachment**](#downloadattachment) | **GET** /v1/attachments/{id}/download | Download a single attachment.|
|[**getAttachment**](#getattachment) | **GET** /v1/attachments/{id} | Get a single attachment.|
|[**listAttachment**](#listattachment) | **GET** /v1/attachments | List all attachments.|
|[**storeAttachment**](#storeattachment) | **POST** /v1/attachments | Store a new attachment.|
|[**updateAttachment**](#updateattachment) | **PUT** /v1/attachments/{id} | Update existing attachment.|
|[**uploadAttachment**](#uploadattachment) | **POST** /v1/attachments/{id}/upload | Upload an attachment.|

# **deleteAttachment**
> deleteAttachment()

With this endpoint you delete an attachment, including any stored file data. 

### Example

```typescript
import {
    AttachmentsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AttachmentsApi(configuration);

let id: string; //The ID of the single attachment. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.deleteAttachment(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the single attachment. | defaults to undefined|
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
|**204** | Attachment deleted. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **downloadAttachment**
> File downloadAttachment()

This endpoint allows you to download the binary content of a transaction. It will be sent to you as a download, using the content type \"application/octet-stream\" and content disposition \"attachment; filename=example.pdf\". 

### Example

```typescript
import {
    AttachmentsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AttachmentsApi(configuration);

let id: string; //The ID of the attachment. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.downloadAttachment(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the attachment. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**File**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The requested attachment |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getAttachment**
> AttachmentSingle getAttachment()

Get a single attachment. This endpoint only returns the available metadata for the attachment. Actual file data is handled in two other endpoints (see below). 

### Example

```typescript
import {
    AttachmentsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AttachmentsApi(configuration);

let id: string; //The ID of the attachment. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getAttachment(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the attachment. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**AttachmentSingle**

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
|**200** | The requested attachment |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listAttachment**
> AttachmentArray listAttachment()

This endpoint lists all attachments. 

### Example

```typescript
import {
    AttachmentsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AttachmentsApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listAttachment(
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

**AttachmentArray**

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
|**200** | A list of attachments. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **storeAttachment**
> AttachmentSingle storeAttachment(attachmentStore)

Creates a new attachment. The data required can be submitted as a JSON body or as a list of parameters. You cannot use this endpoint to upload the actual file data (see below). This endpoint only creates the attachment object. 

### Example

```typescript
import {
    AttachmentsApi,
    Configuration,
    AttachmentStore
} from './api';

const configuration = new Configuration();
const apiInstance = new AttachmentsApi(configuration);

let attachmentStore: AttachmentStore; //JSON array or key=value pairs with the necessary attachment information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.storeAttachment(
    attachmentStore,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **attachmentStore** | **AttachmentStore**| JSON array or key&#x3D;value pairs with the necessary attachment information. See the model for the exact specifications. | |
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**AttachmentSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, application/vnd.api+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | New attachment stored, result in response. |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateAttachment**
> AttachmentSingle updateAttachment(attachmentUpdate)

Update the meta data for an existing attachment. This endpoint does not allow you to upload or download data. For that, see below. 

### Example

```typescript
import {
    AttachmentsApi,
    Configuration,
    AttachmentUpdate
} from './api';

const configuration = new Configuration();
const apiInstance = new AttachmentsApi(configuration);

let id: string; //The ID of the attachment. (default to undefined)
let attachmentUpdate: AttachmentUpdate; //JSON array with updated attachment information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.updateAttachment(
    id,
    attachmentUpdate,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **attachmentUpdate** | **AttachmentUpdate**| JSON array with updated attachment information. See the model for the exact specifications. | |
| **id** | [**string**] | The ID of the attachment. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**AttachmentSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, application/vnd.api+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**200** | Updated attachment stored, result in response |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uploadAttachment**
> uploadAttachment()

Use this endpoint to upload (and possible overwrite) the file contents of an attachment. Simply put the entire file in the body as binary data. 

### Example

```typescript
import {
    AttachmentsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AttachmentsApi(configuration);

let id: string; //The ID of the attachment. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let body: File; // (optional)

const { status, data } = await apiInstance.uploadAttachment(
    id,
    xTraceId,
    body
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **body** | **File**|  | |
| **id** | [**string**] | The ID of the attachment. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

void (empty response body)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/octet-stream
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**204** | Upload was a success |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

