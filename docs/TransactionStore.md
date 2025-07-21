# TransactionStore


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error_if_duplicate_hash** | **boolean** | Break if the submitted transaction exists already. | [optional] [default to undefined]
**apply_rules** | **boolean** | Whether or not to apply rules when submitting transaction. | [optional] [default to undefined]
**fire_webhooks** | **boolean** | Whether or not to fire the webhooks that are related to this event. | [optional] [default to true]
**group_title** | **string** | Title of the transaction if it has been split in more than one piece. Empty otherwise. | [optional] [default to undefined]
**transactions** | [**Array&lt;TransactionSplitStore&gt;**](TransactionSplitStore.md) |  | [default to undefined]

## Example

```typescript
import { TransactionStore } from './api';

const instance: TransactionStore = {
    error_if_duplicate_hash,
    apply_rules,
    fire_webhooks,
    group_title,
    transactions,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
