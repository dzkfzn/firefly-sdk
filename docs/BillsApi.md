# BillsApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteBill**](#deletebill) | **DELETE** /v1/bills/{id} | Delete a bill.|
|[**getBill**](#getbill) | **GET** /v1/bills/{id} | Get a single bill.|
|[**listAttachmentByBill**](#listattachmentbybill) | **GET** /v1/bills/{id}/attachments | List all attachments uploaded to the bill.|
|[**listBill**](#listbill) | **GET** /v1/bills | List all bills.|
|[**listRuleByBill**](#listrulebybill) | **GET** /v1/bills/{id}/rules | List all rules associated with the bill.|
|[**listTransactionByBill**](#listtransactionbybill) | **GET** /v1/bills/{id}/transactions | List all transactions associated with the  bill.|
|[**storeBill**](#storebill) | **POST** /v1/bills | Store a new bill|
|[**updateBill**](#updatebill) | **PUT** /v1/bills/{id} | Update existing bill.|

# **deleteBill**
> deleteBill()

Delete a bill. This will not delete any associated rules. Will not remove associated transactions. WILL remove all associated attachments.

### Example

```typescript
import {
    BillsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BillsApi(configuration);

let id: string; //The ID of the bill. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.deleteBill(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the bill. | defaults to undefined|
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
|**204** | Bill deleted. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getBill**
> BillSingle getBill()

Get a single bill.

### Example

```typescript
import {
    BillsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BillsApi(configuration);

let id: string; //The ID of the bill. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let start: string; //A date formatted YYYY-MM-DD. If it is are added to the request, Firefly III will calculate the appropriate payment and paid dates.  (optional) (default to undefined)
let end: string; //A date formatted YYYY-MM-DD. If it is added to the request, Firefly III will calculate the appropriate payment and paid dates.  (optional) (default to undefined)

const { status, data } = await apiInstance.getBill(
    id,
    xTraceId,
    start,
    end
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the bill. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **start** | [**string**] | A date formatted YYYY-MM-DD. If it is are added to the request, Firefly III will calculate the appropriate payment and paid dates.  | (optional) defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD. If it is added to the request, Firefly III will calculate the appropriate payment and paid dates.  | (optional) defaults to undefined|


### Return type

**BillSingle**

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
|**200** | The requested bill |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listAttachmentByBill**
> AttachmentArray listAttachmentByBill()

This endpoint will list all attachments linked to the bill.

### Example

```typescript
import {
    BillsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BillsApi(configuration);

let id: string; //The ID of the bill. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listAttachmentByBill(
    id,
    xTraceId,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the bill. | defaults to undefined|
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

# **listBill**
> BillArray listBill()

This endpoint will list all the user\'s bills.

### Example

```typescript
import {
    BillsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BillsApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)
let start: string; //A date formatted YYYY-MM-DD. If it is are added to the request, Firefly III will calculate the appropriate payment and paid dates.  (optional) (default to undefined)
let end: string; //A date formatted YYYY-MM-DD. If it is added to the request, Firefly III will calculate the appropriate payment and paid dates.  (optional) (default to undefined)

const { status, data } = await apiInstance.listBill(
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
| **start** | [**string**] | A date formatted YYYY-MM-DD. If it is are added to the request, Firefly III will calculate the appropriate payment and paid dates.  | (optional) defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD. If it is added to the request, Firefly III will calculate the appropriate payment and paid dates.  | (optional) defaults to undefined|


### Return type

**BillArray**

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
|**200** | A list of bills |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listRuleByBill**
> RuleArray listRuleByBill()

This endpoint will list all rules that have an action to set the bill to this bill.

### Example

```typescript
import {
    BillsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BillsApi(configuration);

let id: string; //The ID of the bill. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.listRuleByBill(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the bill. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**RuleArray**

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
|**200** | A list of rules |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listTransactionByBill**
> TransactionArray listTransactionByBill()

This endpoint will list all transactions linked to this bill.

### Example

```typescript
import {
    BillsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BillsApi(configuration);

let id: string; //The ID of the bill. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)
let start: string; //A date formatted YYYY-MM-DD.  (optional) (default to undefined)
let end: string; //A date formatted YYYY-MM-DD.  (optional) (default to undefined)
let type: TransactionTypeFilter; //Optional filter on the transaction type(s) returned (optional) (default to undefined)

const { status, data } = await apiInstance.listTransactionByBill(
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
| **id** | [**string**] | The ID of the bill. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|
| **start** | [**string**] | A date formatted YYYY-MM-DD.  | (optional) defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD.  | (optional) defaults to undefined|
| **type** | **TransactionTypeFilter** | Optional filter on the transaction type(s) returned | (optional) defaults to undefined|


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

# **storeBill**
> BillSingle storeBill(billStore)

Creates a new bill. The data required can be submitted as a JSON body or as a list of parameters.

### Example

```typescript
import {
    BillsApi,
    Configuration,
    BillStore
} from './api';

const configuration = new Configuration();
const apiInstance = new BillsApi(configuration);

let billStore: BillStore; //JSON array or key=value pairs with the necessary bill information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.storeBill(
    billStore,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **billStore** | **BillStore**| JSON array or key&#x3D;value pairs with the necessary bill information. See the model for the exact specifications. | |
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**BillSingle**

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
|**200** | New bill stored, result in response. |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateBill**
> BillSingle updateBill(billUpdate)

Update existing bill.

### Example

```typescript
import {
    BillsApi,
    Configuration,
    BillUpdate
} from './api';

const configuration = new Configuration();
const apiInstance = new BillsApi(configuration);

let id: string; //The ID of the bill. (default to undefined)
let billUpdate: BillUpdate; //JSON array or key=value pairs with updated bill information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.updateBill(
    id,
    billUpdate,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **billUpdate** | **BillUpdate**| JSON array or key&#x3D;value pairs with updated bill information. See the model for the exact specifications. | |
| **id** | [**string**] | The ID of the bill. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**BillSingle**

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
|**200** | Updated bill stored, result in response |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

