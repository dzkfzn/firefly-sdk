# CurrencyExchangeRateStore


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date** | **string** | The date to which the exchange rate is applicable. | [default to undefined]
**rate** | **string** | The exchange rate from the base currency to the destination currency. | [default to undefined]
**from** | **string** | The base currency code. | [default to undefined]
**to** | **string** | The destination currency code. | [default to undefined]

## Example

```typescript
import { CurrencyExchangeRateStore } from './api';

const instance: CurrencyExchangeRateStore = {
    date,
    rate,
    from,
    to,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
