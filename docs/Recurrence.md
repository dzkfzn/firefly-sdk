# Recurrence


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**type** | [**RecurrenceTransactionType**](RecurrenceTransactionType.md) |  | [optional] [default to undefined]
**title** | **string** |  | [optional] [default to undefined]
**description** | **string** | Not to be confused with the description of the actual transaction(s) being created. | [optional] [default to undefined]
**first_date** | **string** | First time the recurring transaction will fire. Must be after today. | [optional] [default to undefined]
**latest_date** | **string** | Last time the recurring transaction has fired. | [optional] [readonly] [default to undefined]
**repeat_until** | **string** | Date until the recurring transaction can fire. Use either this field or repetitions. | [optional] [default to undefined]
**nr_of_repetitions** | **number** | Max number of created transactions. Use either this field or repeat_until. | [optional] [default to undefined]
**apply_rules** | **boolean** | Whether or not to fire the rules after the creation of a transaction. | [optional] [default to undefined]
**active** | **boolean** | If the recurrence is even active. | [optional] [default to undefined]
**notes** | **string** |  | [optional] [default to undefined]
**repetitions** | [**Array&lt;RecurrenceRepetition&gt;**](RecurrenceRepetition.md) |  | [optional] [default to undefined]
**transactions** | [**Array&lt;RecurrenceTransaction&gt;**](RecurrenceTransaction.md) |  | [optional] [default to undefined]

## Example

```typescript
import { Recurrence } from './api';

const instance: Recurrence = {
    created_at,
    updated_at,
    type,
    title,
    description,
    first_date,
    latest_date,
    repeat_until,
    nr_of_repetitions,
    apply_rules,
    active,
    notes,
    repetitions,
    transactions,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
