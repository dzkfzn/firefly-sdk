# RecurrenceUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **string** |  | [optional] [default to undefined]
**description** | **string** | Not to be confused with the description of the actual transaction(s) being created. | [optional] [default to undefined]
**first_date** | **string** | First time the recurring transaction will fire. | [optional] [default to undefined]
**repeat_until** | **string** | Date until the recurring transaction can fire. After that date, it\&#39;s basically inactive. Use either this field or repetitions. | [optional] [default to undefined]
**nr_of_repetitions** | **number** | Max number of created transactions. Use either this field or repeat_until. | [optional] [default to undefined]
**apply_rules** | **boolean** | Whether or not to fire the rules after the creation of a transaction. | [optional] [default to undefined]
**active** | **boolean** | If the recurrence is even active. | [optional] [default to undefined]
**notes** | **string** |  | [optional] [default to undefined]
**repetitions** | [**Array&lt;RecurrenceRepetitionUpdate&gt;**](RecurrenceRepetitionUpdate.md) |  | [optional] [default to undefined]
**transactions** | [**Array&lt;RecurrenceTransactionUpdate&gt;**](RecurrenceTransactionUpdate.md) |  | [optional] [default to undefined]

## Example

```typescript
import { RecurrenceUpdate } from './api';

const instance: RecurrenceUpdate = {
    title,
    description,
    first_date,
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
