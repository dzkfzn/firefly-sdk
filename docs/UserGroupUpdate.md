# UserGroupUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **string** | A descriptive title for the user group. | [default to undefined]
**native_currency_id** | **string** | Use either native_currency_id or native_currency_code. This will set the native currency for the user group (\&#39;financial administration\&#39;). | [optional] [default to undefined]
**native_currency_code** | **string** | Use either native_currency_id or native_currency_code. This will set the native currency for the user group (\&#39;financial administration\&#39;). | [optional] [default to undefined]

## Example

```typescript
import { UserGroupUpdate } from './api';

const instance: UserGroupUpdate = {
    title,
    native_currency_id,
    native_currency_code,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
