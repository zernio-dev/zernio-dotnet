# Zernio.Model.WebhookPayloadWhatsAppTemplateStatusUpdated
Webhook payload for the `whatsapp.template.status_updated` event. Fired when Meta completes (re)review of a template attached to a connected WABA. Maps Meta's `message_template_status_update` field onto our event envelope. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | 
**Event** | **string** |  | 
**Account** | [**WebhookPayloadWhatsAppTemplateStatusUpdatedAccount**](WebhookPayloadWhatsAppTemplateStatusUpdatedAccount.md) |  | 
**Template** | [**WebhookPayloadWhatsAppTemplateStatusUpdatedTemplate**](WebhookPayloadWhatsAppTemplateStatusUpdatedTemplate.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

