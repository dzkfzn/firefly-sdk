# InsightTotalEntry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**difference** | **string** | The amount spent between start date and end date, defined as a string, for this expense account and all asset accounts. | [optional] [default to undefined]
**difference_float** | **number** | The amount spent between start date and end date, defined as a string, for this expense account and all asset accounts. This number is a float (double) and may have rounding errors. | [optional] [default to undefined]
**currency_id** | **string** | The currency ID of the expenses listed for this expense account. | [optional] [default to undefined]
**currency_code** | **string** | The currency code of the expenses listed for this expense account. | [optional] [default to undefined]

## Example

```typescript
import { InsightTotalEntry } from './api';

const instance: InsightTotalEntry = {
    difference,
    difference_float,
    currency_id,
    currency_code,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
