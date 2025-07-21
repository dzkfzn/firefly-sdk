# AutocompletePiggy


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [default to undefined]
**name** | **string** | Name of the piggy bank found by an auto-complete search. | [default to undefined]
**currency_id** | **string** | Currency ID for this piggy bank. This will always be the currency of the piggy bank, never the user\&#39;s native currency. | [optional] [default to undefined]
**currency_code** | **string** | Currency code for this piggy bank. This will always be the currency of the piggy bank, never the user\&#39;s native currency. | [optional] [default to undefined]
**currency_symbol** | **string** |  | [optional] [default to undefined]
**currency_name** | **string** | Currency name for the currency used by this piggy bank. This will always be the currency of the piggy bank, never the user\&#39;s native currency. | [optional] [default to undefined]
**currency_decimal_places** | **number** | Number of decimal places for the currency used by this piggy bank. This will always be the currency of the piggy bank, never the user\&#39;s native currency. | [optional] [default to undefined]
**object_group_id** | **string** | The group ID of the group this object is part of. NULL if no group. | [optional] [default to undefined]
**object_group_title** | **string** | The name of the group. NULL if no group. | [optional] [default to undefined]

## Example

```typescript
import { AutocompletePiggy } from './api';

const instance: AutocompletePiggy = {
    id,
    name,
    currency_id,
    currency_code,
    currency_symbol,
    currency_name,
    currency_decimal_places,
    object_group_id,
    object_group_title,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
