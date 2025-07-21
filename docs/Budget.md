# Budget


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**name** | **string** |  | [default to undefined]
**active** | **boolean** |  | [optional] [default to undefined]
**notes** | **string** |  | [optional] [default to undefined]
**order** | **number** |  | [optional] [readonly] [default to undefined]
**auto_budget_type** | [**AutoBudgetType**](AutoBudgetType.md) |  | [optional] [default to undefined]
**currency_id** | **string** | The currency ID that is part of the budget\&#39;s auto-budget settings, if any. | [optional] [default to undefined]
**currency_code** | **string** | The currency code that is part of the budget\&#39;s auto-budget settings, if any. | [optional] [default to undefined]
**currency_symbol** | **string** | The currency symbol that is part of the budget\&#39;s auto-budget settings, if any. | [optional] [readonly] [default to undefined]
**currency_decimal_places** | **number** | The currency decimal places that is part of the budget\&#39;s auto-budget settings, if any. | [optional] [readonly] [default to undefined]
**native_currency_id** | **string** | The administration\&#39;s native currency ID. | [optional] [readonly] [default to undefined]
**native_currency_code** | **string** | The administration\&#39;s native currency code. | [optional] [readonly] [default to undefined]
**native_currency_symbol** | **string** | The administration\&#39;s native currency symbol. | [optional] [readonly] [default to undefined]
**native_currency_decimal_places** | **number** | The administration\&#39;s native currency decimal places. | [optional] [readonly] [default to undefined]
**auto_budget_amount** | **string** | The amount for the auto-budget, if set. | [optional] [default to undefined]
**native_auto_budget_amount** | **string** | The native amount for the auto-budget, if set. | [optional] [default to undefined]
**auto_budget_period** | [**AutoBudgetPeriod**](AutoBudgetPeriod.md) |  | [optional] [default to undefined]
**spent** | [**Array&lt;BudgetSpent&gt;**](BudgetSpent.md) | Information on how much was spent in this budget. Is only filled in when the start and end date are submitted. | [optional] [readonly] [default to undefined]

## Example

```typescript
import { Budget } from './api';

const instance: Budget = {
    created_at,
    updated_at,
    name,
    active,
    notes,
    order,
    auto_budget_type,
    currency_id,
    currency_code,
    currency_symbol,
    currency_decimal_places,
    native_currency_id,
    native_currency_code,
    native_currency_symbol,
    native_currency_decimal_places,
    auto_budget_amount,
    native_auto_budget_amount,
    auto_budget_period,
    spent,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
