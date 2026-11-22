# Zernio.Model.WebhookPayloadBillingPublishingBlocked

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | 
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Event** | **string** |  | 
**Billing** | [**WebhookPayloadBillingPublishingBlockedBilling**](WebhookPayloadBillingPublishingBlockedBilling.md) |  | 
**BillingUrl** | **string** | Dashboard page where the owner pays or replaces the card. | 
**Timestamp** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

