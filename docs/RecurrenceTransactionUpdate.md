# RecurrenceTransactionUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [default to undefined]
**description** | **string** |  | [optional] [default to undefined]
**amount** | **string** | Amount of the transaction. | [optional] [default to undefined]
**foreign_amount** | **string** | Foreign amount of the transaction. | [optional] [default to undefined]
**currency_id** | **string** | Submit either a currency_id or a currency_code. | [optional] [default to undefined]
**currency_code** | **string** | Submit either a currency_id or a currency_code. | [optional] [default to undefined]
**foreign_currency_id** | **string** | Submit either a foreign_currency_id or a foreign_currency_code, or neither. | [optional] [default to undefined]
**budget_id** | **string** | The budget ID for this transaction. | [optional] [default to undefined]
**category_id** | **string** | Category ID for this transaction. | [optional] [default to undefined]
**source_id** | **string** | ID of the source account. Submit either this or source_name. | [optional] [default to undefined]
**destination_id** | **string** | ID of the destination account. Submit either this or destination_name. | [optional] [default to undefined]
**tags** | **Array&lt;string&gt;** | Array of tags. | [optional] [default to undefined]
**piggy_bank_id** | **string** |  | [optional] [default to undefined]
**bill_id** | **string** | Optional. | [optional] [default to undefined]

## Example

```typescript
import { RecurrenceTransactionUpdate } from './api';

const instance: RecurrenceTransactionUpdate = {
    id,
    description,
    amount,
    foreign_amount,
    currency_id,
    currency_code,
    foreign_currency_id,
    budget_id,
    category_id,
    source_id,
    destination_id,
    tags,
    piggy_bank_id,
    bill_id,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
