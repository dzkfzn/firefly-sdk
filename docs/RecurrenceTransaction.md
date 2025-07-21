# RecurrenceTransaction


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**description** | **string** |  | [default to undefined]
**amount** | **string** | Amount of the transaction. | [default to undefined]
**foreign_amount** | **string** | Foreign amount of the transaction. | [optional] [default to undefined]
**currency_id** | **string** | Submit either a currency_id or a currency_code. | [optional] [default to undefined]
**currency_code** | **string** | Submit either a currency_id or a currency_code. | [optional] [default to undefined]
**currency_symbol** | **string** |  | [optional] [readonly] [default to undefined]
**currency_decimal_places** | **number** | Number of decimals in the currency | [optional] [readonly] [default to undefined]
**foreign_currency_id** | **string** | Submit either a foreign_currency_id or a foreign_currency_code, or neither. | [optional] [default to undefined]
**foreign_currency_code** | **string** | Submit either a foreign_currency_id or a foreign_currency_code, or neither. | [optional] [default to undefined]
**foreign_currency_symbol** | **string** |  | [optional] [readonly] [default to undefined]
**foreign_currency_decimal_places** | **number** | Number of decimals in the currency | [optional] [readonly] [default to undefined]
**budget_id** | **string** | The budget ID for this transaction. | [optional] [default to undefined]
**budget_name** | **string** | The name of the budget to be used. If the budget name is unknown, the ID will be used or the value will be ignored. | [optional] [readonly] [default to undefined]
**category_id** | **string** | Category ID for this transaction. | [optional] [default to undefined]
**category_name** | **string** | Category name for this transaction. | [optional] [default to undefined]
**source_id** | **string** | ID of the source account. Submit either this or source_name. | [optional] [default to undefined]
**source_name** | **string** | Name of the source account. Submit either this or source_id. | [optional] [default to undefined]
**source_iban** | **string** |  | [optional] [readonly] [default to undefined]
**source_type** | [**AccountTypeProperty**](AccountTypeProperty.md) |  | [optional] [default to undefined]
**destination_id** | **string** | ID of the destination account. Submit either this or destination_name. | [optional] [default to undefined]
**destination_name** | **string** | Name of the destination account. Submit either this or destination_id. | [optional] [default to undefined]
**destination_iban** | **string** |  | [optional] [readonly] [default to undefined]
**destination_type** | [**AccountTypeProperty**](AccountTypeProperty.md) |  | [optional] [default to undefined]
**tags** | **Array&lt;string&gt;** | Array of tags. | [optional] [default to undefined]
**piggy_bank_id** | **string** | Optional. Use either this or the piggy_bank_name | [optional] [default to undefined]
**piggy_bank_name** | **string** | Optional. Use either this or the piggy_bank_id | [optional] [default to undefined]
**bill_id** | **string** | Optional. Use either this or the bill_name | [optional] [default to undefined]
**bill_name** | **string** | Optional. Use either this or the bill_id | [optional] [default to undefined]

## Example

```typescript
import { RecurrenceTransaction } from './api';

const instance: RecurrenceTransaction = {
    id,
    description,
    amount,
    foreign_amount,
    currency_id,
    currency_code,
    currency_symbol,
    currency_decimal_places,
    foreign_currency_id,
    foreign_currency_code,
    foreign_currency_symbol,
    foreign_currency_decimal_places,
    budget_id,
    budget_name,
    category_id,
    category_name,
    source_id,
    source_name,
    source_iban,
    source_type,
    destination_id,
    destination_name,
    destination_iban,
    destination_type,
    tags,
    piggy_bank_id,
    piggy_bank_name,
    bill_id,
    bill_name,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
