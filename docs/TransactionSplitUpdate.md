# TransactionSplitUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**transaction_journal_id** | **string** | Transaction journal ID of current transaction (split). | [optional] [default to undefined]
**type** | [**TransactionTypeProperty**](TransactionTypeProperty.md) |  | [optional] [default to undefined]
**date** | **string** | Date of the transaction | [optional] [default to undefined]
**amount** | **string** | Amount of the transaction. | [optional] [default to undefined]
**description** | **string** | Description of the transaction. | [optional] [default to undefined]
**order** | **number** | Order of this entry in the list of transactions. | [optional] [default to undefined]
**currency_id** | **string** | Currency ID. Default is the source account\&#39;s currency, or the user\&#39;s default currency. Can be used instead of currency_code. | [optional] [default to undefined]
**currency_code** | **string** | Currency code. Default is the source account\&#39;s currency, or the user\&#39;s default currency. Can be used instead of currency_id. | [optional] [default to undefined]
**currency_symbol** | **string** |  | [optional] [readonly] [default to undefined]
**currency_name** | **string** |  | [optional] [readonly] [default to undefined]
**currency_decimal_places** | **number** | Number of decimals used in this currency. | [optional] [readonly] [default to undefined]
**foreign_amount** | **string** | The amount in a foreign currency. | [optional] [default to undefined]
**foreign_currency_id** | **string** | Currency ID of the foreign currency. Default is null. Is required when you submit a foreign amount. | [optional] [default to undefined]
**foreign_currency_code** | **string** | Currency code of the foreign currency. Default is NULL. Can be used instead of the foreign_currency_id, but this or the ID is required when submitting a foreign amount. | [optional] [default to undefined]
**foreign_currency_symbol** | **string** |  | [optional] [readonly] [default to undefined]
**foreign_currency_decimal_places** | **number** | Number of decimals in the currency | [optional] [readonly] [default to undefined]
**budget_id** | **string** | The budget ID for this transaction. | [optional] [default to undefined]
**budget_name** | **string** | The name of the budget to be used. If the budget name is unknown, the ID will be used or the value will be ignored. | [optional] [readonly] [default to undefined]
**category_id** | **string** | The category ID for this transaction. | [optional] [default to undefined]
**category_name** | **string** | The name of the category to be used. If the category is unknown, it will be created. If the ID and the name point to different categories, the ID overrules the name. | [optional] [default to undefined]
**source_id** | **string** | ID of the source account. For a withdrawal or a transfer, this must always be an asset account. For deposits, this must be a revenue account. | [optional] [default to undefined]
**source_name** | **string** | Name of the source account. For a withdrawal or a transfer, this must always be an asset account. For deposits, this must be a revenue account. Can be used instead of the source_id. If the transaction is a deposit, the source_name can be filled in freely: the account will be created based on the name. | [optional] [default to undefined]
**source_iban** | **string** |  | [optional] [default to undefined]
**destination_id** | **string** | ID of the destination account. For a deposit or a transfer, this must always be an asset account. For withdrawals this must be an expense account. | [optional] [default to undefined]
**destination_name** | **string** | Name of the destination account. You can submit the name instead of the ID. For everything except transfers, the account will be auto-generated if unknown, so submitting a name is enough. | [optional] [default to undefined]
**destination_iban** | **string** |  | [optional] [default to undefined]
**reconciled** | **boolean** | If the transaction has been reconciled already. When you set this, the amount can no longer be edited by the user. | [optional] [default to undefined]
**bill_id** | **string** | Optional. Use either this or the bill_name | [optional] [default to undefined]
**bill_name** | **string** | Optional. Use either this or the bill_id | [optional] [default to undefined]
**tags** | **Array&lt;string&gt;** | Array of tags. | [optional] [default to undefined]
**notes** | **string** |  | [optional] [default to undefined]
**internal_reference** | **string** | Reference to internal reference of other systems. | [optional] [default to undefined]
**external_id** | **string** | Reference to external ID in other systems. | [optional] [default to undefined]
**external_url** | **string** | External, custom URL for this transaction. | [optional] [default to undefined]
**bunq_payment_id** | **string** | Internal ID of bunq transaction. | [optional] [default to undefined]
**sepa_cc** | **string** | SEPA Clearing Code | [optional] [default to undefined]
**sepa_ct_op** | **string** | SEPA Opposing Account Identifier | [optional] [default to undefined]
**sepa_ct_id** | **string** | SEPA end-to-end Identifier | [optional] [default to undefined]
**sepa_db** | **string** | SEPA mandate identifier | [optional] [default to undefined]
**sepa_country** | **string** | SEPA Country | [optional] [default to undefined]
**sepa_ep** | **string** | SEPA External Purpose indicator | [optional] [default to undefined]
**sepa_ci** | **string** | SEPA Creditor Identifier | [optional] [default to undefined]
**sepa_batch_id** | **string** | SEPA Batch ID | [optional] [default to undefined]
**interest_date** | **string** |  | [optional] [default to undefined]
**book_date** | **string** |  | [optional] [default to undefined]
**process_date** | **string** |  | [optional] [default to undefined]
**due_date** | **string** |  | [optional] [default to undefined]
**payment_date** | **string** |  | [optional] [default to undefined]
**invoice_date** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { TransactionSplitUpdate } from './api';

const instance: TransactionSplitUpdate = {
    transaction_journal_id,
    type,
    date,
    amount,
    description,
    order,
    currency_id,
    currency_code,
    currency_symbol,
    currency_name,
    currency_decimal_places,
    foreign_amount,
    foreign_currency_id,
    foreign_currency_code,
    foreign_currency_symbol,
    foreign_currency_decimal_places,
    budget_id,
    budget_name,
    category_id,
    category_name,
    source_id,
    source_name,
    source_iban,
    destination_id,
    destination_name,
    destination_iban,
    reconciled,
    bill_id,
    bill_name,
    tags,
    notes,
    internal_reference,
    external_id,
    external_url,
    bunq_payment_id,
    sepa_cc,
    sepa_ct_op,
    sepa_ct_id,
    sepa_db,
    sepa_country,
    sepa_ep,
    sepa_ci,
    sepa_batch_id,
    interest_date,
    book_date,
    process_date,
    due_date,
    payment_date,
    invoice_date,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
