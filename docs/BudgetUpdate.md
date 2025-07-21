# BudgetUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [default to undefined]
**active** | **boolean** |  | [optional] [default to undefined]
**order** | **number** |  | [optional] [default to undefined]
**notes** | **string** |  | [optional] [default to undefined]
**auto_budget_type** | [**AutoBudgetType**](AutoBudgetType.md) |  | [optional] [default to undefined]
**auto_budget_currency_id** | **string** | Use either currency_id or currency_code. Defaults to the user\&#39;s default currency. | [optional] [default to undefined]
**auto_budget_currency_code** | **string** | Use either currency_id or currency_code. Defaults to the user\&#39;s default currency. | [optional] [default to undefined]
**auto_budget_amount** | **string** |  | [optional] [default to undefined]
**auto_budget_period** | [**AutoBudgetPeriod**](AutoBudgetPeriod.md) |  | [optional] [default to undefined]

## Example

```typescript
import { BudgetUpdate } from './api';

const instance: BudgetUpdate = {
    name,
    active,
    order,
    notes,
    auto_budget_type,
    auto_budget_currency_id,
    auto_budget_currency_code,
    auto_budget_amount,
    auto_budget_period,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
