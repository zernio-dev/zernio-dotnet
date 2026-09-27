# Zernio.Model.WebhookPayloadAccountAdsInitialSyncCompleted
Webhook payload for `account.ads.initial_sync_completed` events. Fired once per ads-enabled account when the initial discovery + 90-day ad backfill finishes (whether it succeeded fully, partially, or failed). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | 
**Event** | **string** |  | 
**Account** | [**WebhookPayloadAccountAdsInitialSyncCompletedAccount**](WebhookPayloadAccountAdsInitialSyncCompletedAccount.md) |  | 
**Sync** | [**WebhookPayloadAccountAdsInitialSyncCompletedSync**](WebhookPayloadAccountAdsInitialSyncCompletedSync.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

