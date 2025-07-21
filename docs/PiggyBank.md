# PiggyBank


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**name** | **string** |  | [default to undefined]
**accounts** | [**Array&lt;PiggyBankAccountRead&gt;**](PiggyBankAccountRead.md) |  | [optional] [default to undefined]
**currency_id** | **string** |  | [optional] [readonly] [default to undefined]
**currency_code** | **string** |  | [optional] [readonly] [default to undefined]
**currency_symbol** | **string** |  | [optional] [readonly] [default to undefined]
**currency_decimal_places** | **number** | Number of decimals supported by the currency | [optional] [readonly] [default to undefined]
**target_amount** | **string** |  | [default to undefined]
**percentage** | **number** |  | [optional] [readonly] [default to undefined]
**current_amount** | **string** |  | [optional] [default to undefined]
**left_to_save** | **string** |  | [optional] [readonly] [default to undefined]
**save_per_month** | **string** |  | [optional] [readonly] [default to undefined]
**start_date** | **string** | The date you started with this piggy bank. | [optional] [default to undefined]
**target_date** | **string** | The date you intend to finish saving money. | [optional] [default to undefined]
**order** | **number** |  | [optional] [default to undefined]
**active** | **boolean** |  | [optional] [readonly] [default to undefined]
**notes** | **string** |  | [optional] [default to undefined]
**object_group_id** | **string** | The group ID of the group this object is part of. NULL if no group. | [optional] [default to undefined]
**object_group_order** | **number** | The order of the group. At least 1, for the highest sorting. | [optional] [readonly] [default to undefined]
**object_group_title** | **string** | The name of the group. NULL if no group. | [optional] [default to undefined]

## Example

```typescript
import { PiggyBank } from './api';

const instance: PiggyBank = {
    created_at,
    updated_at,
    name,
    accounts,
    currency_id,
    currency_code,
    currency_symbol,
    currency_decimal_places,
    target_amount,
    percentage,
    current_amount,
    left_to_save,
    save_per_month,
    start_date,
    target_date,
    order,
    active,
    notes,
    object_group_id,
    object_group_order,
    object_group_title,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
