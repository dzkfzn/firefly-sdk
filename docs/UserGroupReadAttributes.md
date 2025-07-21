# UserGroupReadAttributes


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**in_use** | **boolean** | Is this user group (\&#39;financial administration\&#39;) currently the active administration? | [optional] [readonly] [default to undefined]
**can_see_members** | **boolean** | Can the current user see the members of this user group? | [optional] [readonly] [default to undefined]
**title** | **string** | Title of the user group. By default, it is the same as the user\&#39;s email address. | [optional] [default to undefined]
**native_currency_id** | **string** | Returns the native currency ID of the user group. | [optional] [readonly] [default to undefined]
**native_currency_code** | **string** | Returns the native currency code of the user group. | [optional] [default to undefined]
**native_currency_symbol** | **string** | Returns the native currency symbol of the user group. | [optional] [readonly] [default to undefined]
**native_currency_decimal_places** | **number** | Returns the native currency decimal places of the user group. | [optional] [readonly] [default to undefined]
**members** | [**Array&lt;UserGroupReadMembers&gt;**](UserGroupReadMembers.md) |  | [optional] [default to undefined]

## Example

```typescript
import { UserGroupReadAttributes } from './api';

const instance: UserGroupReadAttributes = {
    created_at,
    updated_at,
    in_use,
    can_see_members,
    title,
    native_currency_id,
    native_currency_code,
    native_currency_symbol,
    native_currency_decimal_places,
    members,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
