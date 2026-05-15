# Zernio.Model.WebhookPayloadWhatsAppTemplateStatusUpdated
Webhook payload for the `whatsapp.template.status_updated` event. Fired when Meta completes (re)review of a template attached to a connected WABA. Maps Meta's `message_template_status_update` field onto our event envelope. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID | 
**Event** | **string** |  | 
**Account** | [**WebhookPayloadWhatsAppTemplateStatusUpdatedAccount**](WebhookPayloadWhatsAppTemplateStatusUpdatedAccount.md) |  | 
**Template** | [**WebhookPayloadWhatsAppTemplateStatusUpdatedTemplate**](WebhookPayloadWhatsAppTemplateStatusUpdatedTemplate.md) |  | 
**Timestamp** | **DateTime** | ISO-8601 timestamp the webhook was produced. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

