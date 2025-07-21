# RuleTrigger


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [readonly] [default to undefined]
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**type** | [**RuleTriggerKeyword**](RuleTriggerKeyword.md) |  | [default to undefined]
**value** | **string** | The accompanying value the trigger responds to. This value is often mandatory, but this depends on the trigger. | [default to undefined]
**prohibited** | **boolean** | If \&#39;prohibited\&#39; is true, this rule trigger will be negated. \&#39;Description is\&#39; will become \&#39;Description is NOT\&#39; etc. | [optional] [default to false]
**order** | **number** | Order of the trigger | [optional] [readonly] [default to undefined]
**active** | **boolean** | If the trigger is active. Defaults to true. | [optional] [default to true]
**stop_processing** | **boolean** | When true, other triggers will not be checked if this trigger was triggered. Defaults to false. | [optional] [default to false]

## Example

```typescript
import { RuleTrigger } from './api';

const instance: RuleTrigger = {
    id,
    created_at,
    updated_at,
    type,
    value,
    prohibited,
    order,
    active,
    stop_processing,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
