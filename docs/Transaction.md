# Transaction


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**user** | **string** | User ID | [optional] [readonly] [default to undefined]
**group_title** | **string** | Title of the transaction if it has been split in more than one piece. Empty otherwise. | [optional] [default to undefined]
**transactions** | [**Array&lt;TransactionSplit&gt;**](TransactionSplit.md) |  | [default to undefined]

## Example

```typescript
import { Transaction } from './api';

const instance: Transaction = {
    created_at,
    updated_at,
    user,
    group_title,
    transactions,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
