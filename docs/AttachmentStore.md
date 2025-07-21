# AttachmentStore


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**filename** | **string** |  | [default to undefined]
**attachable_type** | [**AttachableType**](AttachableType.md) |  | [default to undefined]
**attachable_id** | **string** | ID of the model this attachment is linked to. | [default to undefined]
**title** | **string** |  | [optional] [default to undefined]
**notes** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { AttachmentStore } from './api';

const instance: AttachmentStore = {
    filename,
    attachable_type,
    attachable_id,
    title,
    notes,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
