# Zernio.Model.WebhookPayloadLead
Webhook payload for lead.received events (Meta Lead Gen / Instant Forms).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID | 
**Event** | **string** |  | 
**Lead** | [**WebhookPayloadLeadLead**](WebhookPayloadLeadLead.md) |  | 
**Account** | [**WebhookPayloadLeadAccount**](WebhookPayloadLeadAccount.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

