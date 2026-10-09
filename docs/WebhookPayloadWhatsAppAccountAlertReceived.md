# Zernio.Model.WebhookPayloadWhatsAppAccountAlertReceived
Webhook payload for `whatsapp.account.alert_received`, forwarded from Meta's `account_alerts` webhook. Alerts about a specific number go to that number's account; business-level alerts go to every connected number on the WABA. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | 
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Event** | **string** |  | 
**Account** | [**WebhookPayloadWhatsAppAccountQualityUpdatedAccount**](WebhookPayloadWhatsAppAccountQualityUpdatedAccount.md) |  | 
**Alert** | [**WebhookPayloadWhatsAppAccountAlertReceivedAlert**](WebhookPayloadWhatsAppAccountAlertReceivedAlert.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

