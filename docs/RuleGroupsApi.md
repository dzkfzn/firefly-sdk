# RuleGroupsApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteRuleGroup**](#deleterulegroup) | **DELETE** /v1/rule-groups/{id} | Delete a rule group.|
|[**fireRuleGroup**](#firerulegroup) | **POST** /v1/rule-groups/{id}/trigger | Fire the rule group on your transactions.|
|[**getRuleGroup**](#getrulegroup) | **GET** /v1/rule-groups/{id} | Get a single rule group.|
|[**listRuleByGroup**](#listrulebygroup) | **GET** /v1/rule-groups/{id}/rules | List rules in this rule group.|
|[**listRuleGroup**](#listrulegroup) | **GET** /v1/rule-groups | List all rule groups.|
|[**storeRuleGroup**](#storerulegroup) | **POST** /v1/rule-groups | Store a new rule group.|
|[**testRuleGroup**](#testrulegroup) | **GET** /v1/rule-groups/{id}/test | Test which transactions would be hit by the rule group. No changes will be made.|
|[**updateRuleGroup**](#updaterulegroup) | **PUT** /v1/rule-groups/{id} | Update existing rule group.|

# **deleteRuleGroup**
> deleteRuleGroup()

Delete a rule group.

### Example

```typescript
import {
    RuleGroupsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new RuleGroupsApi(configuration);

let id: string; //The ID of the rule group. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.deleteRuleGroup(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the rule group. | defaults to undefined|
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
|**204** | Rule group deleted. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **fireRuleGroup**
> fireRuleGroup()

Fire the rule group on your transactions. Changes will be made by the rules in the rule group! Limit the result if you want to.

### Example

```typescript
import {
    RuleGroupsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new RuleGroupsApi(configuration);

let id: string; //The ID of the rule group. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let start: string; //A date formatted YYYY-MM-DD, to limit the transactions the actions will be applied to. Both the start date and the end date must be present.  (optional) (default to undefined)
let end: string; //A date formatted YYYY-MM-DD, to limit the transactions the actions will be applied to. Both the start date and the end date must be present.  (optional) (default to undefined)
let accounts: Array<number>; //Limit the triggering of the rule group to these asset accounts or liabilities. Only asset accounts and liabilities will be accepted. Other types will be silently dropped.  (optional) (default to undefined)

const { status, data } = await apiInstance.fireRuleGroup(
    id,
    xTraceId,
    start,
    end,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the rule group. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **start** | [**string**] | A date formatted YYYY-MM-DD, to limit the transactions the actions will be applied to. Both the start date and the end date must be present.  | (optional) defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD, to limit the transactions the actions will be applied to. Both the start date and the end date must be present.  | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | Limit the triggering of the rule group to these asset accounts or liabilities. Only asset accounts and liabilities will be accepted. Other types will be silently dropped.  | (optional) defaults to undefined|


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
|**204** | The rules in the group are executed. Due to the setup of this function (asynchronous job execution) the result cannot be displayed. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getRuleGroup**
> RuleGroupSingle getRuleGroup()

Get a single rule group. This does not include the rules. For that, see below.

### Example

```typescript
import {
    RuleGroupsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new RuleGroupsApi(configuration);

let id: string; //The ID of the rule group. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.getRuleGroup(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the rule group. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**RuleGroupSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The requested rule group |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listRuleByGroup**
> RuleArray listRuleByGroup()

List rules in this rule group.

### Example

```typescript
import {
    RuleGroupsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new RuleGroupsApi(configuration);

let id: string; //The ID of the rule group. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listRuleByGroup(
    id,
    xTraceId,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the rule group. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|


### Return type

**RuleArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of rules. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listRuleGroup**
> RuleGroupArray listRuleGroup()

List all rule groups.

### Example

```typescript
import {
    RuleGroupsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new RuleGroupsApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listRuleGroup(
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

**RuleGroupArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of rule groups. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **storeRuleGroup**
> RuleGroupSingle storeRuleGroup(ruleGroupStore)

Creates a new rule group. The data required can be submitted as a JSON body or as a list of parameters.

### Example

```typescript
import {
    RuleGroupsApi,
    Configuration,
    RuleGroupStore
} from './api';

const configuration = new Configuration();
const apiInstance = new RuleGroupsApi(configuration);

let ruleGroupStore: RuleGroupStore; //JSON array or key=value pairs with the necessary rule group information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.storeRuleGroup(
    ruleGroupStore,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ruleGroupStore** | **RuleGroupStore**| JSON array or key&#x3D;value pairs with the necessary rule group information. See the model for the exact specifications. | |
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**RuleGroupSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | New rule group stored, result in response. |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **testRuleGroup**
> TransactionArray testRuleGroup()

Test which transactions would be hit by the rule group. No changes will be made. Limit the result if you want to.

### Example

```typescript
import {
    RuleGroupsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new RuleGroupsApi(configuration);

let id: string; //The ID of the rule group. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)
let start: string; //A date formatted YYYY-MM-DD, to limit the transactions the test will be applied to. Both the start date and the end date must be present.  (optional) (default to undefined)
let end: string; //A date formatted YYYY-MM-DD, to limit the transactions the test will be applied to. Both the start date and the end date must be present.  (optional) (default to undefined)
let searchLimit: number; //Maximum number of transactions Firefly III will try. Don\'t set this too high, or it will take Firefly III very long to run the test. I suggest a max of 200.  (optional) (default to undefined)
let triggeredLimit: number; //Maximum number of transactions the rule group can actually trigger on, before Firefly III stops. I would suggest setting this to 10 or 15. Don\'t go above the user\'s page size, because browsing to page 2 or 3 of a test result would fire the test again, making any navigation efforts very slow.  (optional) (default to undefined)
let accounts: Array<number>; //Limit the testing of the rule group to these asset accounts or liabilities. Only asset accounts and liabilities will be accepted. Other types will be silently dropped.  (optional) (default to undefined)

const { status, data } = await apiInstance.testRuleGroup(
    id,
    xTraceId,
    limit,
    page,
    start,
    end,
    searchLimit,
    triggeredLimit,
    accounts
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the rule group. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|
| **start** | [**string**] | A date formatted YYYY-MM-DD, to limit the transactions the test will be applied to. Both the start date and the end date must be present.  | (optional) defaults to undefined|
| **end** | [**string**] | A date formatted YYYY-MM-DD, to limit the transactions the test will be applied to. Both the start date and the end date must be present.  | (optional) defaults to undefined|
| **searchLimit** | [**number**] | Maximum number of transactions Firefly III will try. Don\&#39;t set this too high, or it will take Firefly III very long to run the test. I suggest a max of 200.  | (optional) defaults to undefined|
| **triggeredLimit** | [**number**] | Maximum number of transactions the rule group can actually trigger on, before Firefly III stops. I would suggest setting this to 10 or 15. Don\&#39;t go above the user\&#39;s page size, because browsing to page 2 or 3 of a test result would fire the test again, making any navigation efforts very slow.  | (optional) defaults to undefined|
| **accounts** | **Array&lt;number&gt;** | Limit the testing of the rule group to these asset accounts or liabilities. Only asset accounts and liabilities will be accepted. Other types will be silently dropped.  | (optional) defaults to undefined|


### Return type

**TransactionArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of transactions that would be changed by any of the rules of the rule group. No changes will be made. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateRuleGroup**
> RuleGroupSingle updateRuleGroup(ruleGroupUpdate)

Update existing rule group.

### Example

```typescript
import {
    RuleGroupsApi,
    Configuration,
    RuleGroupUpdate
} from './api';

const configuration = new Configuration();
const apiInstance = new RuleGroupsApi(configuration);

let id: string; //The ID of the rule group. (default to undefined)
let ruleGroupUpdate: RuleGroupUpdate; //JSON array with updated rule group information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.updateRuleGroup(
    id,
    ruleGroupUpdate,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ruleGroupUpdate** | **RuleGroupUpdate**| JSON array with updated rule group information. See the model for the exact specifications. | |
| **id** | [**string**] | The ID of the rule group. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**RuleGroupSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Updated rule group stored, result in response |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

