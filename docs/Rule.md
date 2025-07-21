# Rule


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**title** | **string** |  | [default to undefined]
**description** | **string** |  | [optional] [default to undefined]
**rule_group_id** | **string** | ID of the rule group under which the rule must be stored. Either this field or rule_group_title is mandatory. | [default to undefined]
**rule_group_title** | **string** | Title of the rule group under which the rule must be stored. Either this field or rule_group_id is mandatory. | [optional] [default to undefined]
**order** | **number** |  | [optional] [readonly] [default to undefined]
**trigger** | [**RuleTriggerType**](RuleTriggerType.md) |  | [default to undefined]
**active** | **boolean** | Whether or not the rule is even active. Default is true. | [optional] [default to true]
**strict** | **boolean** | If the rule is set to be strict, ALL triggers must hit in order for the rule to fire. Otherwise, just one is enough. Default value is true. | [optional] [default to undefined]
**stop_processing** | **boolean** | If this value is true and the rule is triggered, other rules  after this one in the group will be skipped. Default value is false. | [optional] [default to false]
**triggers** | [**Array&lt;RuleTrigger&gt;**](RuleTrigger.md) |  | [default to undefined]
**actions** | [**Array&lt;RuleAction&gt;**](RuleAction.md) |  | [default to undefined]

## Example

```typescript
import { Rule } from './api';

const instance: Rule = {
    created_at,
    updated_at,
    title,
    description,
    rule_group_id,
    rule_group_title,
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
