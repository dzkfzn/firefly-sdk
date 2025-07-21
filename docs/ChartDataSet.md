# ChartDataSet


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**label** | **string** | This is the title of the current set. It can refer to an account, a budget or another object (by name). | [optional] [default to undefined]
**currency_id** | **string** | The currency ID of the currency associated to the data in the entries. This may be the native currency of administration. | [optional] [default to undefined]
**currency_code** | **string** |  | [optional] [default to undefined]
**currency_symbol** | **string** |  | [optional] [default to undefined]
**currency_decimal_places** | **number** | Number of decimals for the currency associated to the data in the entries. | [optional] [default to undefined]
**start_date** | **string** |  | [optional] [default to undefined]
**end_date** | **string** |  | [optional] [default to undefined]
**type** | **string** | Indicated the type of chart that is expected to be rendered. You can safely ignore this if you want. | [optional] [default to undefined]
**yAxisID** | **number** | Used to indicate the Y axis for this data set. Is usually between 0 and 1 (left and right side of the chart). | [optional] [default to undefined]
**entries** | [**Array&lt;ChartDataPoint&gt;**](ChartDataPoint.md) | The actual entries for this data set. They \&#39;key\&#39; value is the label for the data point. The value is the actual (numerical) value. | [optional] [default to undefined]

## Example

```typescript
import { ChartDataSet } from './api';

const instance: ChartDataSet = {
    label,
    currency_id,
    currency_code,
    currency_symbol,
    currency_decimal_places,
    start_date,
    end_date,
    type,
    yAxisID,
    entries,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
