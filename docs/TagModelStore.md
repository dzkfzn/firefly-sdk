# TagModelStore


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tag** | **string** | The tag | [default to undefined]
**date** | **string** | The date to which the tag is applicable. | [optional] [default to undefined]
**description** | **string** |  | [optional] [default to undefined]
**latitude** | **number** | Latitude of the tag\&#39;s location, if applicable. Can be used to draw a map. | [optional] [default to undefined]
**longitude** | **number** | Latitude of the tag\&#39;s location, if applicable. Can be used to draw a map. | [optional] [default to undefined]
**zoom_level** | **number** | Zoom level for the map, if drawn. This to set the box right. Unfortunately this is a proprietary value because each map provider has different zoom levels. | [optional] [default to undefined]

## Example

```typescript
import { TagModelStore } from './api';

const instance: TagModelStore = {
    tag,
    date,
    description,
    latitude,
    longitude,
    zoom_level,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
