# WebhookAttempt


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [readonly] [default to undefined]
**updated_at** | **string** |  | [optional] [readonly] [default to undefined]
**webhook_message_id** | **string** | The ID of the webhook message this attempt belongs to. | [optional] [default to undefined]
**status_code** | **number** | The HTTP status code of the error, if any. | [optional] [default to undefined]
**logs** | **string** | Internal log for this attempt. May contain sensitive user data. | [optional] [default to undefined]
**response** | **string** | Webhook receiver response for this attempt, if any. May contain sensitive user data. | [optional] [default to undefined]

## Example

```typescript
import { WebhookAttempt } from './api';

const instance: WebhookAttempt = {
    created_at,
    updated_at,
    webhook_message_id,
    status_code,
    logs,
    response,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
