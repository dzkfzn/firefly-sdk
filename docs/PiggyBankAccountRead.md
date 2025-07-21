# PiggyBankAccountRead


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The ID of the account. | [readonly] [default to undefined]
**name** | **string** |  | [readonly] [default to undefined]
**current_amount** | **string** |  | [default to undefined]
**native_current_amount** | **string** | If convertToNative is on, this will show the amount in the native currency. | [default to undefined]

## Example

```typescript
import { PiggyBankAccountRead } from './api';

const instance: PiggyBankAccountRead = {
    id,
    name,
    current_amount,
    native_current_amount,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
