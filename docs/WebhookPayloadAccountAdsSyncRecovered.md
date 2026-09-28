# Zernio.Model.WebhookPayloadAccountAdsSyncRecovered
Webhook payload for `account.ads.sync_recovered` events. Fired once when an ad account previously reported by `account.ads.sync_failed` syncs successfully again. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. | 
**Event** | **string** |  | 
**Account** | [**WebhookAdsSyncAccount**](WebhookAdsSyncAccount.md) |  | 
**AdAccount** | [**WebhookAdsSyncAdAccount**](WebhookAdsSyncAdAccount.md) |  | 
**Sync** | [**WebhookPayloadAccountAdsSyncRecoveredSync**](WebhookPayloadAccountAdsSyncRecoveredSync.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event. Retries and redeliveries keep the original value. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

