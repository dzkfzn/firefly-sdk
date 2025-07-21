# Category


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**name** | **string** |  | [default to undefined]
**notes** | **string** |  | [optional] [default to undefined]
**native_currency_id** | **string** | The administration\&#39;s native currency ID. | [optional] [readonly] [default to undefined]
**native_currency_code** | **string** | The administration\&#39;s native currency code. | [optional] [readonly] [default to undefined]
**native_currency_symbol** | **string** | The administration\&#39;s native currency symbol. | [optional] [readonly] [default to undefined]
**native_currency_decimal_places** | **number** | The administration\&#39;s native currency decimal places. | [optional] [readonly] [default to undefined]
**spent** | [**Array&lt;CategorySpent&gt;**](CategorySpent.md) |  | [optional] [readonly] [default to undefined]
**earned** | [**Array&lt;CategoryEarned&gt;**](CategoryEarned.md) |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { Category } from './api';

const instance: Category = {
    created_at,
    updated_at,
    name,
    notes,
    native_currency_id,
    native_currency_code,
    native_currency_symbol,
    native_currency_decimal_places,
    spent,
    earned,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
