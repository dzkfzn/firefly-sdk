# RuleTriggerStore


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | [**RuleTriggerKeyword**](RuleTriggerKeyword.md) |  | [default to undefined]
**value** | **string** | The accompanying value the trigger responds to. This value is often mandatory, but this depends on the trigger. | [default to undefined]
**order** | **number** | Order of the trigger | [optional] [default to undefined]
**active** | **boolean** | If the trigger is active. Defaults to true. | [optional] [default to true]
**prohibited** | **boolean** | If \&#39;prohibited\&#39; is true, this rule trigger will be negated. \&#39;Description is\&#39; will become \&#39;Description is NOT\&#39; etc. | [optional] [default to false]
**stop_processing** | **boolean** | When true, other triggers will not be checked if this trigger was triggered. Defaults to false. | [optional] [default to false]

## Example

```typescript
import { RuleTriggerStore } from './api';

const instance: RuleTriggerStore = {
    type,
    value,
    order,
    active,
    prohibited,
    stop_processing,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
