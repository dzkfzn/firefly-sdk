# AutocompleteTransaction


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The ID of a transaction journal (basically a single split). | [default to undefined]
**transaction_group_id** | **string** | The ID of the underlying transaction group. | [optional] [default to undefined]
**name** | **string** | Transaction description | [default to undefined]
**description** | **string** | Transaction description | [default to undefined]

## Example

```typescript
import { AutocompleteTransaction } from './api';

const instance: AutocompleteTransaction = {
    id,
    transaction_group_id,
    name,
    description,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
