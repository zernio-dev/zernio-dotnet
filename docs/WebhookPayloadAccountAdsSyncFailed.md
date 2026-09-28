# Zernio.Model.WebhookPayloadAccountAdsSyncFailed
Webhook payload for `account.ads.sync_failed` events. Fired once per ad account when its ads stop syncing: no successful sync for 24 hours, or every live ad in it at the retry cap. It does not fire again for the same ad account until `account.ads.sync_recovered`. Metrics for the ad account are stale meanwhile. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. | 
**Event** | **string** |  | 
**Account** | [**WebhookAdsSyncAccount**](WebhookAdsSyncAccount.md) |  | 
**AdAccount** | [**WebhookAdsSyncAdAccount**](WebhookAdsSyncAdAccount.md) |  | 
**Sync** | [**WebhookPayloadAccountAdsSyncFailedSync**](WebhookPayloadAccountAdsSyncFailedSync.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event. Retries and redeliveries keep the original value. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

