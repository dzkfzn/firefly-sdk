# PiggyBankEvent


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]
**currency_id** | **string** |  | [optional] [default to undefined]
**currency_code** | **string** |  | [optional] [default to undefined]
**currency_symbol** | **string** |  | [optional] [default to undefined]
**currency_decimal_places** | **number** |  | [optional] [default to undefined]
**amount** | **string** |  | [optional] [default to undefined]
**transaction_journal_id** | **string** | The journal associated with the event. | [optional] [default to undefined]
**transaction_group_id** | **string** | The transaction group associated with the event. | [optional] [default to undefined]

## Example

```typescript
import { PiggyBankEvent } from './api';

const instance: PiggyBankEvent = {
    created_at,
    updated_at,
    currency_id,
    currency_code,
    currency_symbol,
    currency_decimal_places,
    amount,
    transaction_journal_id,
    transaction_group_id,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
