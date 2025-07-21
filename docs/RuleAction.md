# RuleAction


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [readonly] [default to undefined]
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**type** | [**RuleActionKeyword**](RuleActionKeyword.md) |  | [default to undefined]
**value** | **string** | The accompanying value the action will set, change or update. Can be empty, but for some types this value is mandatory. | [default to undefined]
**order** | **number** | Order of the action | [optional] [default to undefined]
**active** | **boolean** | If the action is active. Defaults to true. | [optional] [default to true]
**stop_processing** | **boolean** | When true, other actions will not be fired after this action has fired. Defaults to false. | [optional] [default to false]

## Example

```typescript
import { RuleAction } from './api';

const instance: RuleAction = {
    id,
    created_at,
    updated_at,
    type,
    value,
    order,
    active,
    stop_processing,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
