# CurrencyExchangeRateReadAttributes


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**from_currency_id** | **string** | Base currency ID for this exchange rate entry. | [optional] [readonly] [default to undefined]
**from_currency_code** | **string** | Base currency code for this exchange rate entry. | [optional] [readonly] [default to undefined]
**from_currency_symbol** | **string** | Base currency symbol for this exchange rate entry. | [optional] [readonly] [default to undefined]
**from_currency_decimal_places** | **number** | Base currency decimal places for this exchange rate entry. | [optional] [readonly] [default to undefined]
**to_currency_id** | **string** | Destination currency ID for this exchange rate entry. | [optional] [readonly] [default to undefined]
**to_currency_code** | **string** | Destination currency code for this exchange rate entry. | [optional] [readonly] [default to undefined]
**to_currency_symbol** | **string** | Destination currency symbol for this exchange rate entry. | [optional] [readonly] [default to undefined]
**to_currency_decimal_places** | **number** | Destination currency decimal places for this exchange rate entry. | [optional] [readonly] [default to undefined]
**rate** | **string** | The actual exchange rate. How many \&#39;to\&#39; currency will you get for 1 \&#39;from\&#39; currency? | [optional] [readonly] [default to undefined]
**date** | **string** | Date and time of the exchange rate. | [optional] [readonly] [default to undefined]

## Example

```typescript
import { CurrencyExchangeRateReadAttributes } from './api';

const instance: CurrencyExchangeRateReadAttributes = {
    created_at,
    updated_at,
    from_currency_id,
    from_currency_code,
    from_currency_symbol,
    from_currency_decimal_places,
    to_currency_id,
    to_currency_code,
    to_currency_symbol,
    to_currency_decimal_places,
    rate,
    date,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
