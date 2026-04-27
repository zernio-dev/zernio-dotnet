# Zernio.Model.WebhookPayloadAccountAdsInitialSyncCompleted
Webhook payload for `account.ads.initial_sync_completed` events. Fired once per ads-enabled account when the initial discovery + 90-day ad backfill finishes (whether it succeeded fully, partially, or failed). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID | 
**Event** | **string** |  | 
**Account** | [**WebhookPayloadAccountAdsInitialSyncCompletedAccount**](WebhookPayloadAccountAdsInitialSyncCompletedAccount.md) |  | 
**Sync** | [**WebhookPayloadAccountAdsInitialSyncCompletedSync**](WebhookPayloadAccountAdsInitialSyncCompletedSync.md) |  | 
**Timestamp** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

