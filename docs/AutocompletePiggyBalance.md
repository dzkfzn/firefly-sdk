# AutocompletePiggyBalance


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [default to undefined]
**name** | **string** | Name of the piggy bank found by an auto-complete search. | [default to undefined]
**name_with_balance** | **string** | Name of the piggy bank found by an auto-complete search, including the currently saved amount and the target amount. | [optional] [default to undefined]
**currency_id** | **string** | Currency ID for the currency used by this piggy bank. This will always be the piggy bank\&#39;s currency, never the native currency. | [optional] [default to undefined]
**currency_code** | **string** | Currency code for the currency used by this piggy bank. This will always be the piggy bank\&#39;s currency, never the native currency. | [optional] [default to undefined]
**currency_symbol** | **string** | Currency symbol for the currency used by this piggy bank. This will always be the piggy bank\&#39;s currency, never the native currency. | [optional] [default to undefined]
**currency_decimal_places** | **number** | Currency decimal places for the currency used by this piggy bank. This will always be the piggy bank\&#39;s currency, never the native currency. | [optional] [default to undefined]
**object_group_id** | **string** | The group ID of the group this object is part of. NULL if no group. | [optional] [default to undefined]
**object_group_title** | **string** | The name of the group. NULL if no group. | [optional] [default to undefined]

## Example

```typescript
import { AutocompletePiggyBalance } from './api';

const instance: AutocompletePiggyBalance = {
    id,
    name,
    name_with_balance,
    currency_id,
    currency_code,
    currency_symbol,
    currency_decimal_places,
    object_group_id,
    object_group_title,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
