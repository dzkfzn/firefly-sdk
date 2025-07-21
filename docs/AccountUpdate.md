# AccountUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [default to undefined]
**iban** | **string** |  | [optional] [default to undefined]
**bic** | **string** |  | [optional] [default to undefined]
**account_number** | **string** |  | [optional] [default to undefined]
**opening_balance** | **string** |  | [optional] [default to undefined]
**opening_balance_date** | **string** |  | [optional] [default to undefined]
**virtual_balance** | **string** |  | [optional] [default to undefined]
**currency_id** | **string** | Use either currency_id or currency_code. Defaults to the user\&#39;s default currency. | [optional] [default to undefined]
**currency_code** | **string** | Use either currency_id or currency_code. Defaults to the user\&#39;s default currency. | [optional] [default to undefined]
**active** | **boolean** | If omitted, defaults to true. | [optional] [default to true]
**order** | **number** | Order of the account | [optional] [default to undefined]
**include_net_worth** | **boolean** | If omitted, defaults to true. | [optional] [default to true]
**account_role** | [**AccountRoleProperty**](AccountRoleProperty.md) |  | [optional] [default to undefined]
**credit_card_type** | [**CreditCardTypeProperty**](CreditCardTypeProperty.md) |  | [optional] [default to undefined]
**monthly_payment_date** | **string** | Mandatory when the account_role is ccAsset. Moment at which CC payment installments are asked for by the bank. | [optional] [default to undefined]
**liability_type** | [**LiabilityTypeProperty**](LiabilityTypeProperty.md) |  | [optional] [default to undefined]
**interest** | **string** | Mandatory when type is liability. Interest percentage. | [optional] [default to undefined]
**interest_period** | [**InterestPeriodProperty**](InterestPeriodProperty.md) |  | [optional] [default to undefined]
**notes** | **string** |  | [optional] [default to undefined]
**latitude** | **number** | Latitude of the account\&#39;s location, if applicable. Can be used to draw a map. If omitted, the existing location will be kept. If submitted as NULL, the current location will be removed. | [optional] [default to undefined]
**longitude** | **number** | Latitude of the account\&#39;s location, if applicable. Can be used to draw a map. If omitted, the existing location will be kept. If submitted as NULL, the current location will be removed. | [optional] [default to undefined]
**zoom_level** | **number** | Zoom level for the map, if drawn. This to set the box right. Unfortunately this is a proprietary value because each map provider has different zoom levels. If omitted, the existing location will be kept. If submitted as NULL, the current location will be removed. | [optional] [default to undefined]

## Example

```typescript
import { AccountUpdate } from './api';

const instance: AccountUpdate = {
    name,
    iban,
    bic,
    account_number,
    opening_balance,
    opening_balance_date,
    virtual_balance,
    currency_id,
    currency_code,
    active,
    order,
    include_net_worth,
    account_role,
    credit_card_type,
    monthly_payment_date,
    liability_type,
    interest,
    interest_period,
    notes,
    latitude,
    longitude,
    zoom_level,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
