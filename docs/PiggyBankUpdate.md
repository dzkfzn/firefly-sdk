# PiggyBankUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [optional] [default to undefined]
**accounts** | [**Array&lt;PiggyBankAccountUpdate&gt;**](PiggyBankAccountUpdate.md) |  | [optional] [default to undefined]
**currency_id** | **string** |  | [optional] [readonly] [default to undefined]
**currency_code** | **string** |  | [optional] [readonly] [default to undefined]
**target_amount** | **string** |  | [optional] [default to undefined]
**start_date** | **string** | The date you started with this piggy bank. | [optional] [default to undefined]
**target_date** | **string** | The date you intend to finish saving money. | [optional] [default to undefined]
**order** | **number** |  | [optional] [default to undefined]
**active** | **boolean** |  | [optional] [readonly] [default to undefined]
**notes** | **string** |  | [optional] [default to undefined]
**object_group_id** | **string** | The group ID of the group this object is part of. NULL if no group. | [optional] [default to undefined]
**object_group_title** | **string** | The name of the group. NULL if no group. | [optional] [default to undefined]

## Example

```typescript
import { PiggyBankUpdate } from './api';

const instance: PiggyBankUpdate = {
    name,
    accounts,
    currency_id,
    currency_code,
    target_amount,
    start_date,
    target_date,
    order,
    active,
    notes,
    object_group_id,
    object_group_title,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
