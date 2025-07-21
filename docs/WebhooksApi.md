# WebhooksApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteWebhook**](#deletewebhook) | **DELETE** /v1/webhooks/{id} | Delete a webhook.|
|[**deleteWebhookMessage**](#deletewebhookmessage) | **DELETE** /v1/webhooks/{id}/messages/{messageId} | Delete a webhook message.|
|[**deleteWebhookMessageAttempt**](#deletewebhookmessageattempt) | **DELETE** /v1/webhooks/{id}/messages/{messageId}/attempts/{attemptId} | Delete a webhook attempt.|
|[**getSingleWebhookMessage**](#getsinglewebhookmessage) | **GET** /v1/webhooks/{id}/messages/{messageId} | Get a single message from a webhook.|
|[**getSingleWebhookMessageAttempt**](#getsinglewebhookmessageattempt) | **GET** /v1/webhooks/{id}/messages/{messageId}/attempts/{attemptId} | Get a single failed attempt from a single webhook message.|
|[**getWebhook**](#getwebhook) | **GET** /v1/webhooks/{id} | Get a single webhook.|
|[**getWebhookMessageAttempts**](#getwebhookmessageattempts) | **GET** /v1/webhooks/{id}/messages/{messageId}/attempts | Get all the failed attempts of a single webhook message.|
|[**getWebhookMessages**](#getwebhookmessages) | **GET** /v1/webhooks/{id}/messages | Get all the messages of a single webhook.|
|[**listWebhook**](#listwebhook) | **GET** /v1/webhooks | List all webhooks.|
|[**storeWebhook**](#storewebhook) | **POST** /v1/webhooks | Store a new webhook|
|[**submitWebook**](#submitwebook) | **POST** /v1/webhooks/{id}/submit | Submit messages for a webhook.|
|[**triggerTransactionWebhook**](#triggertransactionwebhook) | **POST** /v1/webhooks/{id}/trigger-transaction/{transactionId} | Trigger webhook for a given transaction.|
|[**updateWebhook**](#updatewebhook) | **PUT** /v1/webhooks/{id} | Update existing webhook.|

# **deleteWebhook**
> deleteWebhook()

Delete a webhook.

### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let id: string; //The webhook ID. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.deleteWebhook(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The webhook ID. | defaults to undefined|
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
|**204** | Webhook deleted. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteWebhookMessage**
> deleteWebhookMessage()

Delete a webhook message. Any time a webhook is triggered the message is stored before it\'s sent. You can delete them before or after sending.

### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let id: string; //The webhook ID. (default to undefined)
let messageId: number; //The webhook message ID. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.deleteWebhookMessage(
    id,
    messageId,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The webhook ID. | defaults to undefined|
| **messageId** | [**number**] | The webhook message ID. | defaults to undefined|
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
|**204** | Webhook message deleted. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteWebhookMessageAttempt**
> deleteWebhookMessageAttempt()

Delete a webhook message attempt. If you delete all attempts for a webhook message, Firefly III will (once again) assume all is well with the webhook message and will try to send it again.

### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let id: string; //The webhook ID. (default to undefined)
let messageId: number; //The webhook message ID. (default to undefined)
let attemptId: number; //The webhook message attempt ID. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.deleteWebhookMessageAttempt(
    id,
    messageId,
    attemptId,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The webhook ID. | defaults to undefined|
| **messageId** | [**number**] | The webhook message ID. | defaults to undefined|
| **attemptId** | [**number**] | The webhook message attempt ID. | defaults to undefined|
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
|**204** | Webhook message attempt deleted. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getSingleWebhookMessage**
> WebhookMessageSingle getSingleWebhookMessage()

When a webhook is triggered it will store the actual content of the webhook in a webhook message. You can view and analyse a single one using this endpoint.

### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let id: string; //The webhook ID. (default to undefined)
let messageId: number; //The webhook message ID. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getSingleWebhookMessage(
    id,
    messageId,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The webhook ID. | defaults to undefined|
| **messageId** | [**number**] | The webhook message ID. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**WebhookMessageSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A single webhook message. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getSingleWebhookMessageAttempt**
> WebhookAttemptSingle getSingleWebhookMessageAttempt()

When a webhook message fails to send it will store the failure in an \"attempt\". You can view and analyse these. Webhooks messages that receive too many attempts (failures) will not be fired. You must first clear out old attempts and try again. This endpoint shows you the details of a single attempt. The ID of the attempt must match the corresponding webhook and webhook message.

### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let id: string; //The webhook ID. (default to undefined)
let messageId: number; //The webhook message ID. (default to undefined)
let attemptId: number; //The webhook attempt ID. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getSingleWebhookMessageAttempt(
    id,
    messageId,
    attemptId,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The webhook ID. | defaults to undefined|
| **messageId** | [**number**] | The webhook message ID. | defaults to undefined|
| **attemptId** | [**number**] | The webhook attempt ID. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**WebhookAttemptSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A single webhook attempt. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getWebhook**
> WebhookSingle getWebhook()

Gets all info of a single webhook.

### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let id: string; //The webhook ID. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getWebhook(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The webhook ID. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**WebhookSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The requested webhook. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getWebhookMessageAttempts**
> WebhookAttemptArray getWebhookMessageAttempts()

When a webhook message fails to send it will store the failure in an \"attempt\". You can view and analyse these. Webhook messages that receive too many attempts (failures) will not be sent again. You must first clear out old attempts before the message can go out again.

### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let id: string; //The webhook ID. (default to undefined)
let messageId: number; //The webhook message ID. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.getWebhookMessageAttempts(
    id,
    messageId,
    xTraceId,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The webhook ID. | defaults to undefined|
| **messageId** | [**number**] | The webhook message ID. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|


### Return type

**WebhookAttemptArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of webhook attempts. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getWebhookMessages**
> WebhookMessageArray getWebhookMessages()

When a webhook is triggered the actual message that will be send is stored in a \"message\". You can view and analyse these messages.

### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let id: string; //The webhook ID. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getWebhookMessages(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The webhook ID. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**WebhookMessageArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of webhook messages. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listWebhook**
> WebhookArray listWebhook()

List all the user\'s webhooks.

### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listWebhook(
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

**WebhookArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of webhooks. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **storeWebhook**
> WebhookSingle storeWebhook(webhookStore)

Creates a new webhook. The data required can be submitted as a JSON body or as a list of parameters. The webhook will be given a random secret. 

### Example

```typescript
import {
    WebhooksApi,
    Configuration,
    WebhookStore
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let webhookStore: WebhookStore; //JSON array or key=value pairs with the necessary webhook information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.storeWebhook(
    webhookStore,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **webhookStore** | **WebhookStore**| JSON array or key&#x3D;value pairs with the necessary webhook information. See the model for the exact specifications. | |
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**WebhookSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | New webhook stored, result in response. |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **submitWebook**
> submitWebook()

This endpoint will submit any open messages for this webhook. This is an asynchronous operation, so you can\'t see the result. Refresh the webhook message and/or the webhook message attempts to see the results. This may take some time if the webhook receiver is slow.

### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let id: string; //The webhook ID. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.submitWebook(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The webhook ID. | defaults to undefined|
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
|**400** | Bad request |  -  |
|**200** | OK! |  -  |
|**204** | No messages to send, so did nothing. |  -  |
|**404** | Page not found |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **triggerTransactionWebhook**
> triggerTransactionWebhook()

This endpoint will execute this webhook for a given transaction ID. This is an asynchronous operation, so you can\'t see the result. Refresh the webhook message and/or the webhook message attempts to see the results. This may take some time if the webhook receiver is slow.

### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let id: string; //The webhook ID. (default to undefined)
let transactionId: string; //The transaction ID. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.triggerTransactionWebhook(
    id,
    transactionId,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The webhook ID. | defaults to undefined|
| **transactionId** | [**string**] | The transaction ID. | defaults to undefined|
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
|**400** | Bad request |  -  |
|**204** | Webhook triggered successfully. |  -  |
|**404** | Page not found |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateWebhook**
> WebhookSingle updateWebhook(webhookUpdate)

Update an existing webhook\'s information. If you wish to reset the secret, submit any value as the \"secret\". Firefly III will take this as a hint and reset the secret of the webhook.

### Example

```typescript
import {
    WebhooksApi,
    Configuration,
    WebhookUpdate
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let id: string; //The webhook ID. (default to undefined)
let webhookUpdate: WebhookUpdate; //JSON array with updated webhook information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.updateWebhook(
    id,
    webhookUpdate,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **webhookUpdate** | **WebhookUpdate**| JSON array with updated webhook information. See the model for the exact specifications. | |
| **id** | [**string**] | The webhook ID. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**WebhookSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Updated webhook stored, result in response |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

