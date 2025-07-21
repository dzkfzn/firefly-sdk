# CurrencyStore


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **boolean** | Defaults to true | [optional] [default to true]
**_default** | **boolean** | Make this currency the default currency. You can set this value to FALSE, in which case nothing will change to the default currency. If you set it to TRUE, the current default currency will no longer be the default currency. | [optional] [default to undefined]
**code** | **string** |  | [default to undefined]
**name** | **string** |  | [default to undefined]
**symbol** | **string** |  | [default to undefined]
**decimal_places** | **number** | Supports 0-16 decimals. | [optional] [default to undefined]

## Example

```typescript
import { CurrencyStore } from './api';

const instance: CurrencyStore = {
    enabled,
    _default,
    code,
    name,
    symbol,
    decimal_places,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
