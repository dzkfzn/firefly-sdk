# CurrencyUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **boolean** | If the currency is enabled | [optional] [default to undefined]
**_default** | **boolean** | If the currency must be the default for the user. You can only submit TRUE. Submitting FALSE will not drop this currency as the default currency, because then the system would be without one. | [optional] [default to undefined]
**code** | **string** | The currency code | [optional] [default to undefined]
**name** | **string** | The currency name | [optional] [default to undefined]
**symbol** | **string** | The currency symbol | [optional] [default to undefined]
**decimal_places** | **number** | How many decimals to use when displaying this currency. Between 0 and 16. | [optional] [default to undefined]

## Example

```typescript
import { CurrencyUpdate } from './api';

const instance: CurrencyUpdate = {
    enabled,
    _default,
    code,
    name,
    symbol,
    decimal_places,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
