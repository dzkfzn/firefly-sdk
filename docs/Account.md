# Account


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**active** | **boolean** | If omitted, defaults to true. | [optional] [default to true]
**order** | **number** | Order of the account. Is NULL if account is not asset or liability. | [optional] [default to undefined]
**name** | **string** |  | [default to undefined]
**type** | [**ShortAccountTypeProperty**](ShortAccountTypeProperty.md) |  | [default to undefined]
**account_role** | [**AccountRoleProperty**](AccountRoleProperty.md) |  | [optional] [default to undefined]
**currency_id** | **string** | Use either currency_id or currency_code. Defaults to the user\&#39;s default currency. | [optional] [default to undefined]
**currency_code** | **string** | Use either currency_id or currency_code. Defaults to the user\&#39;s default currency. | [optional] [default to undefined]
**currency_symbol** | **string** |  | [optional] [readonly] [default to undefined]
**currency_decimal_places** | **number** |  | [optional] [readonly] [default to undefined]
**native_currency_id** | **string** | Returns the native currency ID of the administration. | [optional] [readonly] [default to undefined]
**native_currency_code** | **string** | Returns the native currency code of the administration. | [optional] [default to undefined]
**native_currency_symbol** | **string** | Returns the native currency symbol of the administration. | [optional] [readonly] [default to undefined]
**native_currency_decimal_places** | **number** | Returns the native currency decimal places of the administration. | [optional] [readonly] [default to undefined]
**current_balance** | **string** | The current balance of the account in the account\&#39;s currency OR the native currency if the account has no currency. | [optional] [readonly] [default to undefined]
**native_current_balance** | **string** | The current balance of the account in the administration\&#39;s native currency. | [optional] [readonly] [default to undefined]
**current_balance_date** | **string** | The timestamp for this date is always 23:59:59, to indicate it\&#39;s the balance at the very END of that particular day. | [optional] [readonly] [default to undefined]
**notes** | **string** |  | [optional] [default to undefined]
**monthly_payment_date** | **string** | Mandatory when the account_role is ccAsset. Moment at which CC payment installments are asked for by the bank. | [optional] [default to undefined]
**credit_card_type** | [**CreditCardTypeProperty**](CreditCardTypeProperty.md) |  | [optional] [default to undefined]
**account_number** | **string** |  | [optional] [default to undefined]
**iban** | **string** |  | [optional] [default to undefined]
**bic** | **string** |  | [optional] [default to undefined]
**virtual_balance** | **string** | The virtual balance of the account in the account\&#39;s currency or the administration\&#39;s native currency if the account has no currency. | [optional] [default to undefined]
**native_virtual_balance** | **string** | The virtual balance of the account in administration\&#39;s native currency. | [optional] [default to undefined]
**opening_balance** | **string** | Represents the opening balance, the initial amount this account holds in the currency of the account or the administration\&#39;s native currency if the account has no currency. | [optional] [default to undefined]
**native_opening_balance** | **string** | Represents the opening balance, in the administration\&#39;s native currency. | [optional] [default to undefined]
**opening_balance_date** | **string** | Represents the date of the opening balance. | [optional] [default to undefined]
**liability_type** | [**LiabilityTypeProperty**](LiabilityTypeProperty.md) |  | [optional] [default to undefined]
**liability_direction** | [**LiabilityDirectionProperty**](LiabilityDirectionProperty.md) |  | [optional] [default to undefined]
**interest** | **string** | Mandatory when type is liability. Interest percentage. | [optional] [default to undefined]
**interest_period** | [**InterestPeriodProperty**](InterestPeriodProperty.md) |  | [optional] [default to undefined]
**current_debt** | **string** | Represents the current debt for liabilities. | [optional] [default to undefined]
**include_net_worth** | **boolean** | If omitted, defaults to true. | [optional] [default to true]
**longitude** | **number** | Latitude of the accounts\&#39;s location, if applicable. Can be used to draw a map. | [optional] [default to undefined]
**latitude** | **number** | Latitude of the accounts\&#39;s location, if applicable. Can be used to draw a map. | [optional] [default to undefined]
**zoom_level** | **number** | Zoom level for the map, if drawn. This to set the box right. Unfortunately this is a proprietary value because each map provider has different zoom levels. | [optional] [default to undefined]

## Example

```typescript
import { Account } from './api';

const instance: Account = {
    created_at,
    updated_at,
    active,
    order,
    name,
    type,
    account_role,
    currency_id,
    currency_code,
    currency_symbol,
    currency_decimal_places,
    native_currency_id,
    native_currency_code,
    native_currency_symbol,
    native_currency_decimal_places,
    current_balance,
    native_current_balance,
    current_balance_date,
    notes,
    monthly_payment_date,
    credit_card_type,
    account_number,
    iban,
    bic,
    virtual_balance,
    native_virtual_balance,
    opening_balance,
    native_opening_balance,
    opening_balance_date,
    liability_type,
    liability_direction,
    interest,
    interest_period,
    current_debt,
    include_net_worth,
    longitude,
    latitude,
    zoom_level,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
