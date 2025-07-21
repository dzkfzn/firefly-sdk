# WebhookStore


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**active** | **boolean** | Boolean to indicate if the webhook is active | [optional] [default to undefined]
**title** | **string** | A title for the webhook for easy recognition. | [default to undefined]
**trigger** | [**WebhookTrigger**](WebhookTrigger.md) |  | [default to undefined]
**response** | [**WebhookResponse**](WebhookResponse.md) |  | [default to undefined]
**delivery** | [**WebhookDelivery**](WebhookDelivery.md) |  | [default to undefined]
**url** | **string** | The URL of the webhook. Has to start with &#x60;https&#x60;. | [default to undefined]

## Example

```typescript
import { WebhookStore } from './api';

const instance: WebhookStore = {
    active,
    title,
    trigger,
    response,
    delivery,
    url,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
