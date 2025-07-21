# User


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**email** | **string** | The new users email address. | [default to undefined]
**blocked** | **boolean** | Boolean to indicate if the user is blocked. | [optional] [default to undefined]
**blocked_code** | [**UserBlockedCodeProperty**](UserBlockedCodeProperty.md) |  | [optional] [default to undefined]
**role** | [**UserRoleProperty**](UserRoleProperty.md) |  | [optional] [default to undefined]

## Example

```typescript
import { User } from './api';

const instance: User = {
    created_at,
    updated_at,
    email,
    blocked,
    blocked_code,
    role,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
