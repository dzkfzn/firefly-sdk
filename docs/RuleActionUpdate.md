# RuleActionUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | [**RuleActionKeyword**](RuleActionKeyword.md) |  | [optional] [default to undefined]
**value** | **string** | The accompanying value the action will set, change or update. Can be empty, but for some types this value is mandatory. | [optional] [default to undefined]
**order** | **number** | Order of the action | [optional] [default to undefined]
**active** | **boolean** | If the action is active. | [optional] [default to undefined]
**stop_processing** | **boolean** | When true, other actions will not be fired after this action has fired. | [optional] [default to undefined]

## Example

```typescript
import { RuleActionUpdate } from './api';

const instance: RuleActionUpdate = {
    type,
    value,
    order,
    active,
    stop_processing,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
