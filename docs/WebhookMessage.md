# WebhookMessage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**sent** | **boolean** | If this message is sent yet. | [optional] [default to undefined]
**errored** | **boolean** | If this message has errored out. | [optional] [default to undefined]
**webhook_id** | **string** | The ID of the webhook this message belongs to. | [optional] [default to undefined]
**uuid** | **string** | Long UUID string for identification of this webhook message. | [optional] [default to undefined]
**message** | **string** | The actual message that is sent or will be sent as JSON string. | [optional] [default to undefined]

## Example

```typescript
import { WebhookMessage } from './api';

const instance: WebhookMessage = {
    created_at,
    updated_at,
    sent,
    errored,
    webhook_id,
    uuid,
    message,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
