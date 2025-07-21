# RuleTriggerUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | [**RuleTriggerKeyword**](RuleTriggerKeyword.md) |  | [optional] [default to undefined]
**value** | **string** | The accompanying value the trigger responds to. This value is often mandatory, but this depends on the trigger. If the rule trigger is something like \&#39;has any tag\&#39;, submit the string \&#39;true\&#39;. | [optional] [default to undefined]
**order** | **number** | Order of the trigger | [optional] [default to undefined]
**active** | **boolean** | If the trigger is active. | [optional] [default to undefined]
**stop_processing** | **boolean** | When true, other triggers will not be checked if this trigger was triggered. | [optional] [default to undefined]

## Example

```typescript
import { RuleTriggerUpdate } from './api';

const instance: RuleTriggerUpdate = {
    type,
    value,
    order,
    active,
    stop_processing,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
