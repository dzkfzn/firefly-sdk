# TransactionLinkUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**link_type_id** | **string** | The link type ID to use. Use this field OR use the link_type_name field. | [optional] [default to undefined]
**link_type_name** | **string** | The link type name to use. Use this field OR use the link_type_id field. | [optional] [default to undefined]
**inward_id** | **string** | The inward transaction transaction_journal_id for the link. This becomes the \&#39;is paid by\&#39; transaction of the set. | [optional] [default to undefined]
**outward_id** | **string** | The outward transaction transaction_journal_id for the link. This becomes the \&#39;pays for\&#39; transaction of the set. | [optional] [default to undefined]
**notes** | **string** | Optional. Some notes. If you submit an empty string the current notes will be removed | [optional] [default to undefined]

## Example

```typescript
import { TransactionLinkUpdate } from './api';

const instance: TransactionLinkUpdate = {
    link_type_id,
    link_type_name,
    inward_id,
    outward_id,
    notes,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
