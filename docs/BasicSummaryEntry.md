# BasicSummaryEntry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **string** | This is a reference to the type of info shared, not influenced by translations or user preferences. The EUR value is a reference to the currency code. Possibilities are: balance-in-ABC, spent-in-ABC, earned-in-ABC, bills-paid-in-ABC, bills-unpaid-in-ABC, left-to-spend-in-ABC and net-worth-in-ABC. | [optional] [default to undefined]
**title** | **string** | A translated title for the information shared. | [optional] [default to undefined]
**monetary_value** | **number** | The amount as a float. | [optional] [default to undefined]
**currency_id** | **string** | The currency ID of the associated currency. | [optional] [default to undefined]
**currency_code** | **string** |  | [optional] [default to undefined]
**currency_symbol** | **string** |  | [optional] [default to undefined]
**currency_decimal_places** | **number** | Number of decimals for the associated currency. | [optional] [default to undefined]
**no_available_budgets** | **boolean** | True if there are no available budgets available. | [optional] [default to undefined]
**value_parsed** | **string** | The amount formatted according to the users locale | [optional] [default to undefined]
**local_icon** | **string** | Reference to a font-awesome icon without the fa- part. | [optional] [default to undefined]
**sub_title** | **string** | A short explanation of the amounts origin. Already formatted according to the locale of the user or translated, if relevant. | [optional] [default to undefined]

## Example

```typescript
import { BasicSummaryEntry } from './api';

const instance: BasicSummaryEntry = {
    key,
    title,
    monetary_value,
    currency_id,
    currency_code,
    currency_symbol,
    currency_decimal_places,
    no_available_budgets,
    value_parsed,
    local_icon,
    sub_title,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
