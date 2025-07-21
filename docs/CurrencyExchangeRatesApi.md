# CurrencyExchangeRatesApi

All URIs are relative to *https://demo.firefly-iii.org/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteSpecificCurrencyExchangeRate**](#deletespecificcurrencyexchangerate) | **DELETE** /v1/exchange-rates/{id} | Delete a specific currency exchange rate.|
|[**deleteSpecificCurrencyExchangeRates**](#deletespecificcurrencyexchangerates) | **DELETE** /v1/exchange-rates/rates/{from}/{to} | Delete all currency exchange rates from \&#39;from\&#39; to \&#39;to\&#39;.|
|[**listCurrencyExchangeRates**](#listcurrencyexchangerates) | **GET** /v1/exchange-rates | List all exchange rates.|
|[**listSpecificCurrencyExchangeRate**](#listspecificcurrencyexchangerate) | **GET** /v1/exchange-rates/{id} | List a single specific exchange rate.|
|[**listSpecificCurrencyExchangeRates**](#listspecificcurrencyexchangerates) | **GET** /v1/exchange-rates/rates/{from}/{to} | List all exchange rate from/to the mentioned currencies.|
|[**storeCurrencyExchangeRate**](#storecurrencyexchangerate) | **POST** /v1/exchange-rates | Store a new currency exchange rate.|

# **deleteSpecificCurrencyExchangeRate**
> deleteSpecificCurrencyExchangeRate()

Delete a specific currency exchange rate.

### Example

```typescript
import {
    CurrencyExchangeRatesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrencyExchangeRatesApi(configuration);

let id: string; //The ID of the requested currency exchange rate. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.deleteSpecificCurrencyExchangeRate(
    id,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the requested currency exchange rate. | defaults to undefined|
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
|**204** | Currency exchange rate deleted. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteSpecificCurrencyExchangeRates**
> deleteSpecificCurrencyExchangeRates()

Delete all currency exchange rates from \'from\' to \'to\' on a specific date or today.

### Example

```typescript
import {
    CurrencyExchangeRatesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrencyExchangeRatesApi(configuration);

let from: string; //The currency code of the \'from\' currency. (default to undefined)
let to: string; //The currency code of the \'to\' currency. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let date: string; //A date formatted YYYY-MM-DD. Defaults to today.  (optional) (default to undefined)

const { status, data } = await apiInstance.deleteSpecificCurrencyExchangeRates(
    from,
    to,
    xTraceId,
    date
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **from** | [**string**] | The currency code of the \&#39;from\&#39; currency. | defaults to undefined|
| **to** | [**string**] | The currency code of the \&#39;to\&#39; currency. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **date** | [**string**] | A date formatted YYYY-MM-DD. Defaults to today.  | (optional) defaults to undefined|


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
|**204** | Currency exchange rate(s) deleted. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listCurrencyExchangeRates**
> CurrencyExchangeRateArray listCurrencyExchangeRates()

List exchange rates.

### Example

```typescript
import {
    CurrencyExchangeRatesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrencyExchangeRatesApi(configuration);

let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listCurrencyExchangeRates(
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

**CurrencyExchangeRateArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of all available currency exchange rates. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listSpecificCurrencyExchangeRate**
> CurrencyExchangeRateSingle listSpecificCurrencyExchangeRate()

List a single specific exchange rate

### Example

```typescript
import {
    CurrencyExchangeRatesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrencyExchangeRatesApi(configuration);

let id: string; //The ID of the requested currency exchange rate. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listSpecificCurrencyExchangeRate(
    id,
    xTraceId,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The ID of the requested currency exchange rate. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|


### Return type

**CurrencyExchangeRateSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of currency exchange rates. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listSpecificCurrencyExchangeRates**
> CurrencyExchangeRateArray listSpecificCurrencyExchangeRates()

List all exchange rate from/to the mentioned currencies.

### Example

```typescript
import {
    CurrencyExchangeRatesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrencyExchangeRatesApi(configuration);

let from: string; //The currency code of the \'from\' currency. (default to undefined)
let to: string; //The currency code of the \'to\' currency. (default to undefined)
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)
let limit: number; //Number of items per page. The default pagination is per 50 items. (optional) (default to undefined)
let page: number; //Page number. The default pagination is per 50 items. (optional) (default to undefined)

const { status, data } = await apiInstance.listSpecificCurrencyExchangeRates(
    from,
    to,
    xTraceId,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **from** | [**string**] | The currency code of the \&#39;from\&#39; currency. | defaults to undefined|
| **to** | [**string**] | The currency code of the \&#39;to\&#39; currency. | defaults to undefined|
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|
| **limit** | [**number**] | Number of items per page. The default pagination is per 50 items. | (optional) defaults to undefined|
| **page** | [**number**] | Page number. The default pagination is per 50 items. | (optional) defaults to undefined|


### Return type

**CurrencyExchangeRateArray**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | A list of currency exchange rates. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **storeCurrencyExchangeRate**
> CurrencyExchangeRateSingle storeCurrencyExchangeRate(currencyExchangeRateStore)

Stores a new exchange rate. The data required can be submitted as a JSON body or as a list of parameters.

### Example

```typescript
import {
    CurrencyExchangeRatesApi,
    Configuration,
    CurrencyExchangeRateStore
} from './api';

const configuration = new Configuration();
const apiInstance = new CurrencyExchangeRatesApi(configuration);

let currencyExchangeRateStore: CurrencyExchangeRateStore; //JSON array or key=value pairs with the necessary category information. See the model for the exact specifications.
let xTraceId: string; //Unique identifier associated with this request. (optional) (default to undefined)

const { status, data } = await apiInstance.storeCurrencyExchangeRate(
    currencyExchangeRateStore,
    xTraceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **currencyExchangeRateStore** | **CurrencyExchangeRateStore**| JSON array or key&#x3D;value pairs with the necessary category information. See the model for the exact specifications. | |
| **xTraceId** | [**string**] | Unique identifier associated with this request. | (optional) defaults to undefined|


### Return type

**CurrencyExchangeRateSingle**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | New category stored, result in response. |  -  |
|**422** | Validation error. The body will have the exact details. |  -  |
|**401** | Unauthenticated |  -  |
|**404** | Page not found |  -  |
|**400** | Bad request |  -  |
|**500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

