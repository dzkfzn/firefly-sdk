# InsightTransferEntry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | This ID is a reference to the original object. | [optional] [default to undefined]
**name** | **string** | This is the name of the object. | [optional] [default to undefined]
**difference** | **string** | The total amount transferred between start date and end date, a number defined as a string, for this asset account. | [optional] [default to undefined]
**difference_float** | **number** | The total amount transferred between start date and end date, a number as a float, for this asset account. May have rounding errors. | [optional] [default to undefined]
**_in** | **string** | The total amount transferred TO this account between start date and end date, a number defined as a string, for this asset account. | [optional] [default to undefined]
**in_float** | **number** | The total amount transferred FROM this account between start date and end date, a number as a float, for this asset account. May have rounding errors. | [optional] [default to undefined]
**out** | **string** | The total amount transferred FROM this account between start date and end date, a number defined as a string, for this asset account. | [optional] [default to undefined]
**out_float** | **number** | The total amount transferred TO this account between start date and end date, a number as a float, for this asset account. May have rounding errors. | [optional] [default to undefined]
**currency_id** | **string** | The currency ID of the expenses listed for this account. | [optional] [default to undefined]
**currency_code** | **string** | The currency code of the expenses listed for this account. | [optional] [default to undefined]

## Example

```typescript
import { InsightTransferEntry } from './api';

const instance: InsightTransferEntry = {
    id,
    name,
    difference,
    difference_float,
    _in,
    in_float,
    out,
    out_float,
    currency_id,
    currency_code,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
