# CronResultRow


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**job_fired** | **boolean** | This value tells you if this specific cron job actually fired. It may not fire. Some cron jobs only fire every 24 hours, for example.  | [optional] [default to undefined]
**job_succeeded** | **boolean** | This value tells you if this specific cron job actually did something. The job may fire but not change anything.  | [optional] [default to undefined]
**job_errored** | **boolean** | If the cron job ran into some kind of an error, this value will be true. | [optional] [default to undefined]
**message** | **string** | If the cron job ran into some kind of an error, this value will be the error message. The success message if the job actually ran OK.  | [optional] [default to undefined]

## Example

```typescript
import { CronResultRow } from './api';

const instance: CronResultRow = {
    job_fired,
    job_succeeded,
    job_errored,
    message,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
