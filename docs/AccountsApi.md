# AccountsApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteAccount**](#deleteaccount) | **DELETE** /v1/accounts/{id} | Permanently delete account.|
|[**getAccount**](#getaccount) | **GET** /v1/accounts/{id} | Get single account.|
|[**listAccount**](#listaccount) | **GET** /v1/accounts | List all accounts.|
|[**listAttachmentByAccount**](#listattachmentbyaccount) | **GET** /v1/accounts/{id}/attachments | Lists all attachments.|
|[**listPiggyBankByAccount**](#listpiggybankbyaccount) | **GET** /v1/accounts/{id}/piggy-banks | List all piggy banks related to the account.|
|[**listTransactionByAccount**](#listtransactionbyaccount) | **GET** /v1/accounts/{id}/transactions | List all transactions related to the account.|
|[**storeAccount**](#storeaccount) | **POST** /v1/accounts | Create new account.|
|[**updateAccount**](#updateaccount) | **PUT** /v1/accounts/{id} | Update existing account.|

# **deleteAccount**
> deleteAccount()

Will permanently delete an account. Any associated transactions and piggy banks are ALSO deleted. Cannot be recovered from. 

### Example

```typescript
import {
    AccountsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AccountsApi(configuration);

let id: string; //The ID of the account. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.deleteAccount(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the account. | defaults to undefined|
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
|**204** | Account deleted |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getAccount**
> AccountSingle getAccount()

Returns a single account by its ID. 

### Example

```typescript
import {
    AccountsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AccountsApi(configuration);

let id: string; //The ID of the account. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let date: string; //A date formatted YYYY-MM-DD. When added to the request, Firefly III will show the account\'s balance on that day.  (optional) (default to undefined)

const { status, data } = await apiInstance.getAccount(
    id,
    xTraceId,
    date
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the account. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **date** | [**string**] | A date formatted YYYY-MM-DD. When added to the request, Firefly III will show the account\&#39;s balance on that day.  | (optional) defaults to undefined|


### Return type

**AccountSingle**

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
|**200** | The requested account |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listAccount**
> AccountArray listAccount()

This endpoint returns a list of all the accounts owned by the authenticated user. 

### Example

```typescript
import {
    AccountsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AccountsApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)
let date: string; //A date formatted YYYY-MM-DD. When added to the request, Firefly III will show the account\'s balance on that day.  (optional) (default to undefined)
let type: AccountTypeFilter; //Optional filter on the account type(s) returned (optional) (default to undefined)

const { status, data } = await apiInstance.listAccount(
    xTraceId,
    limit,
    page,
    date,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|
| **date** | [**string**] | A date formatted YYYY-MM-DD. When added to the request, Firefly III will show the account\&#39;s balance on that day.  | (optional) defaults to undefined|
| **type** | **AccountTypeFilter** | Optional filter on the account type(s) returned | (optional) defaults to undefined|


### Return type

**AccountArray**

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
|**200** | A list of accounts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listAttachmentByAccount**
> AttachmentArray listAttachmentByAccount()

Lists all attachments.

### Example

```typescript
import {
    AccountsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AccountsApi(configuration);

let id: string; //The ID of the account. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listAttachmentByAccount(
    id,
    xTraceId,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the account. | defaults to undefined|
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
|**200** | A list of attachments |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listPiggyBankByAccount**
> PiggyBankArray listPiggyBankByAccount()

This endpoint returns a list of all the piggy banks connected to the account. 

### Example

```typescript
import {
    AccountsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AccountsApi(configuration);

let id: string; //The ID of the account. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listPiggyBankByAccount(
    id,
    xTraceId,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the account. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|


### Return type

**PiggyBankArray**

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
|**200** | A list of piggy banks |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listTransactionByAccount**
> TransactionArray listTransactionByAccount()

This endpoint returns a list of all the transactions connected to the account. 

### Example

```typescript
import {
    AccountsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AccountsApi(configuration);

let id: string; //The ID of the account. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)
let start: string; //A date formatted YYYY-MM-DD.  (optional) (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (optional) (default to undefined)
let type: TransactionTypeFilter; //Optional filter on the transaction type(s) returned. (optional) (default to undefined)

const { status, data } = await apiInstance.listTransactionByAccount(
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
| **id** | [**string**] | The ID of the account. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | (optional) defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | (optional) defaults to undefined|
| **type** | **TransactionTypeFilter** | Optional filter on the transaction type(s) returned. | (optional) defaults to undefined|


### Return type

**TransactionArray**

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
|**200** | A list of transactions |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **storeAccount**
> AccountSingle storeAccount(accountStore)

Creates a new account. The data required can be submitted as a JSON body or as a list of parameters (in key=value pairs, like a webform).

### Example

```typescript
import {
    AccountsApi,
    Configuration,
    AccountStore
} from './api';

const configuration = new Configuration();
const apiInstance = new AccountsApi(configuration);

let accountStore: AccountStore; //JSON array with the necessary account information or key=value pairs. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.storeAccount(
    accountStore,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **accountStore** | **AccountStore**| JSON array with the necessary account information or key&#x3D;value pairs. See the model for the exact specifications. | |
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**AccountSingle**

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
|**422** | Validation error. The body will have the exact details. |  -  |
|**200** | New account stored, result in response. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateAccount**
> AccountSingle updateAccount(accountUpdate)

Used to update a single account. All fields that are not submitted will be cleared (set to NULL). The model will tell you which fields are mandatory. 

### Example

```typescript
import {
    AccountsApi,
    Configuration,
    AccountUpdate
} from './api';

const configuration = new Configuration();
const apiInstance = new AccountsApi(configuration);

let id: string; //The ID of the account. (default to undefined)
let accountUpdate: AccountUpdate; //JSON array or formdata with updated account information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.updateAccount(
    id,
    accountUpdate,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **accountUpdate** | **AccountUpdate**| JSON array or formdata with updated account information. See the model for the exact specifications. | |
| **id** | [**string**] | The ID of the account. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**AccountSingle**

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
|**422** | Validation error. The body will have the exact details. |  -  |
|**200** | Updated account stored, result in response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

