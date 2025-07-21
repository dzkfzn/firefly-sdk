# PiggyBankStore


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [default to undefined]
**accounts** | [**Array&lt;PiggyBankAccountStore&gt;**](PiggyBankAccountStore.md) |  | [optional] [default to undefined]
**target_amount** | **string** |  | [default to undefined]
**current_amount** | **string** |  | [optional] [default to undefined]
**start_date** | **string** | The date you started with this piggy bank. | [optional] [default to undefined]
**target_date** | **string** | The date you intend to finish saving money. | [optional] [default to undefined]
**order** | **number** |  | [optional] [default to undefined]
**active** | **boolean** |  | [optional] [readonly] [default to undefined]
**notes** | **string** |  | [optional] [default to undefined]
**object_group_id** | **string** | The group ID of the group this object is part of. NULL if no group. | [optional] [default to undefined]
**object_group_title** | **string** | The name of the group. NULL if no group. | [optional] [default to undefined]

## Example

```typescript
import { PiggyBankStore } from './api';

const instance: PiggyBankStore = {
    name,
    accounts,
    target_amount,
    current_amount,
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
