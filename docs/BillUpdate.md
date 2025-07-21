# BillUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency_id** | **string** | Use either currency_id or currency_code | [optional] [default to undefined]
**currency_code** | **string** | Use either currency_id or currency_code | [optional] [default to undefined]
**name** | **string** |  | [default to undefined]
**amount_min** | **string** |  | [optional] [default to undefined]
**amount_max** | **string** |  | [optional] [default to undefined]
**date** | **string** |  | [optional] [default to undefined]
**end_date** | **string** | The date after which this bill is no longer valid or applicable | [optional] [default to undefined]
**extension_date** | **string** | The date before which the bill must be renewed (or cancelled) | [optional] [default to undefined]
**repeat_freq** | [**BillRepeatFrequency**](BillRepeatFrequency.md) |  | [optional] [default to undefined]
**skip** | **number** | How often the bill must be skipped. 1 means a bi-monthly bill. | [optional] [default to undefined]
**active** | **boolean** | If the bill is active. | [optional] [default to undefined]
**notes** | **string** |  | [optional] [default to undefined]
**object_group_id** | **string** | The group ID of the group this object is part of. NULL if no group. | [optional] [default to undefined]
**object_group_title** | **string** | The name of the group. NULL if no group. | [optional] [default to undefined]

## Example

```typescript
import { BillUpdate } from './api';

const instance: BillUpdate = {
    currency_id,
    currency_code,
    name,
    amount_min,
    amount_max,
    date,
    end_date,
    extension_date,
    repeat_freq,
    skip,
    active,
    notes,
    object_group_id,
    object_group_title,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
