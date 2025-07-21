# Currency


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**enabled** | **boolean** | Defaults to true | [optional] [default to true]
**_default** | **boolean** | Make this currency the native currency. | [optional] [default to undefined]
**_native** | **boolean** | Make this currency the native currency. | [optional] [default to undefined]
**code** | **string** |  | [default to undefined]
**name** | **string** |  | [default to undefined]
**symbol** | **string** |  | [default to undefined]
**decimal_places** | **number** | Supports 0-16 decimals. | [optional] [default to undefined]

## Example

```typescript
import { Currency } from './api';

const instance: Currency = {
    created_at,
    updated_at,
    enabled,
    _default,
    _native,
    code,
    name,
    symbol,
    decimal_places,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
