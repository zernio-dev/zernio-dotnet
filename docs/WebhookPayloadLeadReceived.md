# Zernio.Model.WebhookPayloadLeadReceived
Webhook payload for the lead.received event. Fired when a Meta Lead Gen Form receives a new submission. Real-time delivery requires the page to be subscribed to the `leadgen` webhook field — Zernio subscribes on connect; existing accounts get backfilled by `scripts/backfill-fb-webhook-subscriptions.ts`.  Requires the Ads add-on. Subscribers without the add-on are filtered at delivery time. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID | 
**Event** | **string** |  | 
**Lead** | [**Lead**](Lead.md) |  | 
**Account** | [**WebhookPayloadLeadReceivedAccount**](WebhookPayloadLeadReceivedAccount.md) |  | 
**Timestamp** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

