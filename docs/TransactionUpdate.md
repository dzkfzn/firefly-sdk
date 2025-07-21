# TransactionUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**apply_rules** | **boolean** | Whether or not to apply rules when submitting transaction. | [optional] [default to undefined]
**fire_webhooks** | **boolean** | Whether or not to fire the webhooks that are related to this event. | [optional] [default to true]
**group_title** | **string** | Title of the transaction if it has been split in more than one piece. Empty otherwise. | [optional] [default to undefined]
**transactions** | [**Array&lt;TransactionSplitUpdate&gt;**](TransactionSplitUpdate.md) |  | [optional] [default to undefined]

## Example

```typescript
import { TransactionUpdate } from './api';

const instance: TransactionUpdate = {
    apply_rules,
    fire_webhooks,
    group_title,
    transactions,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
