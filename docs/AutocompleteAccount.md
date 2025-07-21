# AutocompleteAccount


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [default to undefined]
**name** | **string** | Name of the account found by an auto-complete search. | [default to undefined]
**name_with_balance** | **string** | Asset accounts and liabilities have a second field with the given date\&#39;s account balance in the account currency or native currency. | [default to undefined]
**type** | **string** | Account type of the account found by the auto-complete search. | [default to undefined]
**currency_id** | **string** | ID for the currency used by this account. If the user prefers amounts converted to their native currency, this native currency is used instead. | [default to undefined]
**currency_name** | **string** | Currency name for the currency used by this account. If the user prefers amounts converted to their native currency, this native currency is used instead. | [default to undefined]
**currency_code** | **string** | Currency code for the currency used by this account. If the user prefers amounts converted to their native currency, this native currency is used instead. | [default to undefined]
**currency_symbol** | **string** | Currency symbol for the currency used by this account. If the user prefers amounts converted to their native currency, this native currency is used instead. | [default to undefined]
**currency_decimal_places** | **number** | Number of decimal places for the currency used by this account. If the user prefers amounts converted to their native currency, this native currency is used instead. | [default to undefined]
**account_currency_id** | **string** | ID for the currency used by this account. Even if \&quot;convertToNative\&quot; is on, the account currency ID is displayed here. | [optional] [default to undefined]
**account_currency_name** | **string** | Name for the currency used by this account. Even if \&quot;convertToNative\&quot; is on, the account currency name is displayed here. | [optional] [default to undefined]
**account_currency_code** | **string** | Code for the currency used by this account. Even if \&quot;convertToNative\&quot; is on, the account currency code is displayed here. | [optional] [default to undefined]
**account_currency_symbol** | **string** | Code for the currency used by this account. Even if \&quot;convertToNative\&quot; is on, the account currency code is displayed here. | [optional] [default to undefined]
**account_currency_decimal_places** | **number** | Number of decimal places for the currency used by this account. Even if \&quot;convertToNative\&quot; is on, the account currency code is displayed here. | [optional] [default to undefined]

## Example

```typescript
import { AutocompleteAccount } from './api';

const instance: AutocompleteAccount = {
    id,
    name,
    name_with_balance,
    type,
    currency_id,
    currency_name,
    currency_code,
    currency_symbol,
    currency_decimal_places,
    account_currency_id,
    account_currency_name,
    account_currency_code,
    account_currency_symbol,
    account_currency_decimal_places,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
