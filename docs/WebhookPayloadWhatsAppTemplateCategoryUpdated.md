# Zernio.Model.WebhookPayloadWhatsAppTemplateCategoryUpdated
Webhook payload for the `whatsapp.template.category_updated` event. Fired when Meta reclassifies a template's category attached to a connected WABA. Maps Meta's `template_category_update` field onto our event envelope. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID | 
**Event** | **string** |  | 
**Account** | [**WebhookPayloadWhatsAppTemplateStatusUpdatedAccount**](WebhookPayloadWhatsAppTemplateStatusUpdatedAccount.md) |  | 
**Template** | [**WebhookPayloadWhatsAppTemplateCategoryUpdatedTemplate**](WebhookPayloadWhatsAppTemplateCategoryUpdatedTemplate.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

