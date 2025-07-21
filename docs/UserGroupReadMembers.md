# UserGroupReadMembers


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | **string** | The ID of the member. | [optional] [readonly] [default to undefined]
**user_email** | **string** | The email address of the member | [optional] [readonly] [default to undefined]
**you** | **boolean** | Is this you? (the current user) | [optional] [readonly] [default to undefined]
**roles** | [**Set&lt;UserGroupReadRole&gt;**](UserGroupReadRole.md) |  | [optional] [default to undefined]

## Example

```typescript
import { UserGroupReadMembers } from './api';

const instance: UserGroupReadMembers = {
    user_id,
    user_email,
    you,
    roles,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
