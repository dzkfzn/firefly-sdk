# AvailableBudget


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**currency_id** | **string** | Use either currency_id or currency_code. | [optional] [default to undefined]
**currency_code** | **string** | Use either currency_id or currency_code. | [optional] [default to undefined]
**currency_symbol** | **string** |  | [optional] [readonly] [default to undefined]
**currency_decimal_places** | **number** |  | [optional] [readonly] [default to undefined]
**native_currency_id** | **string** | The currency ID of the administration\&#39;s native currency. | [optional] [readonly] [default to undefined]
**native_currency_code** | **string** | The currency code of the administration\&#39;s native currency. | [optional] [readonly] [default to undefined]
**native_currency_symbol** | **string** | The currency symbol of the administration\&#39;s native currency. | [optional] [readonly] [default to undefined]
**native_currency_decimal_places** | **number** | The currency decimal places of the administration\&#39;s native currency. | [optional] [readonly] [default to undefined]
**amount** | **string** |  | [default to undefined]
**native_amount** | **string** | The amount of this available budget in the native currency of this administration. | [optional] [default to undefined]
**start** | **string** | Start date of the available budget. | [default to undefined]
**end** | **string** | End date of the available budget. | [default to undefined]
**spent_in_budgets** | [**Array&lt;BudgetSpent&gt;**](BudgetSpent.md) |  | [optional] [readonly] [default to undefined]
**spent_outside_budget** | [**Array&lt;BudgetSpent&gt;**](BudgetSpent.md) |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { AvailableBudget } from './api';

const instance: AvailableBudget = {
    created_at,
    updated_at,
    currency_id,
    currency_code,
    currency_symbol,
    currency_decimal_places,
    native_currency_id,
    native_currency_code,
    native_currency_symbol,
    native_currency_decimal_places,
    amount,
    native_amount,
    start,
    end,
    spent_in_budgets,
    spent_outside_budget,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
