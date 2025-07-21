# Attachment


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**attachable_type** | [**AttachableType**](AttachableType.md) |  | [default to undefined]
**attachable_id** | **string** | ID of the model this attachment is linked to. | [default to undefined]
**md5** | **string** | MD5 hash of the file for basic duplicate detection. This field is deprecated. | [optional] [default to undefined]
**hash** | **string** | Hash of the file for basic duplicate detection. It\&#39;s still md5 lol. | [optional] [default to undefined]
**filename** | **string** |  | [default to undefined]
**download_url** | **string** |  | [optional] [default to undefined]
**upload_url** | **string** |  | [optional] [default to undefined]
**title** | **string** |  | [optional] [default to undefined]
**notes** | **string** |  | [optional] [default to undefined]
**mime** | **string** |  | [optional] [readonly] [default to undefined]
**size** | **number** |  | [optional] [readonly] [default to undefined]

## Example

```typescript
import { Attachment } from './api';

const instance: Attachment = {
    created_at,
    updated_at,
    attachable_type,
    attachable_id,
    md5,
    hash,
    filename,
    download_url,
    upload_url,
    title,
    notes,
    mime,
    size,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
