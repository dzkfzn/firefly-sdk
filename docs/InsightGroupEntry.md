# InsightGroupEntry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | This ID is a reference to the original object. | [optional] [default to undefined]
**name** | **string** | This is the name of the object. | [optional] [default to undefined]
**difference** | **string** | The amount spent or earned between start date and end date, a number defined as a string, for this object and all asset accounts. | [optional] [default to undefined]
**difference_float** | **number** | The amount spent or earned between start date and end date, a number as a float, for this object and all asset accounts. May have rounding errors. | [optional] [default to undefined]
**currency_id** | **string** | The currency ID of the expenses listed for this account. | [optional] [default to undefined]
**currency_code** | **string** | The currency code of the expenses listed for this account. | [optional] [default to undefined]

## Example

```typescript
import { InsightGroupEntry } from './api';

const instance: InsightGroupEntry = {
    id,
    name,
    difference,
    difference_float,
    currency_id,
    currency_code,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
