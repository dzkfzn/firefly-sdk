# RuleUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **string** |  | [optional] [default to undefined]
**description** | **string** |  | [optional] [default to undefined]
**rule_group_id** | **string** | ID of the rule group under which the rule must be stored. Either this field or rule_group_title is mandatory. | [optional] [default to undefined]
**order** | **number** |  | [optional] [default to undefined]
**trigger** | [**RuleTriggerType**](RuleTriggerType.md) |  | [optional] [default to undefined]
**active** | **boolean** | Whether or not the rule is even active. Default is true. | [optional] [default to true]
**strict** | **boolean** | If the rule is set to be strict, ALL triggers must hit in order for the rule to fire. Otherwise, just one is enough. Default value is true. | [optional] [default to undefined]
**stop_processing** | **boolean** | If this value is true and the rule is triggered, other rules  after this one in the group will be skipped. Default value is false. | [optional] [default to false]
**triggers** | [**Array&lt;RuleTriggerUpdate&gt;**](RuleTriggerUpdate.md) |  | [optional] [default to undefined]
**actions** | [**Array&lt;RuleActionUpdate&gt;**](RuleActionUpdate.md) |  | [optional] [default to undefined]

## Example

```typescript
import { RuleUpdate } from './api';

const instance: RuleUpdate = {
    title,
    description,
    rule_group_id,
    order,
    trigger,
    active,
    strict,
    stop_processing,
    triggers,
    actions,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
