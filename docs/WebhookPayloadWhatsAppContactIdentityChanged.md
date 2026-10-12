# Zernio.Model.WebhookPayloadWhatsAppContactIdentityChanged
Webhook payload for the `whatsapp.contact.identity_changed` event. Fired when Meta reports that a WhatsApp user is now known by a different identifier: a `system` message of type `user_changed_number`, `user_changed_user_id` or `user_identity_changed`, or a `user_id_update` webhook (BSUID regenerated). Zernio re-keys the inbox conversation and contact channel before firing. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | 
**Profiles** | [**List&lt;WebhookProfilesInner&gt;**](WebhookProfilesInner.md) | The profiles this event belongs to, each with the externalId you set on it (null when none is set). Present on every event tied to a profile and absent on events that belong to none. Events spanning several profiles (a post published to accounts of different profiles) list each once. Use it to route the event to your tenant without storing Zernio profile ids. | [optional] 
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Event** | **string** |  | 
**Account** | [**WebhookPayloadWhatsAppAccountQualityUpdatedAccount**](WebhookPayloadWhatsAppAccountQualityUpdatedAccount.md) |  | 
**Reason** | **string** | Which Meta signal reported the change. &#x60;user_changed_number&#x60;: new phone number. &#x60;user_changed_user_id&#x60; and &#x60;user_id_update&#x60;: new BSUID. | 
**Previous** | [**WhatsAppContactIdentity**](WhatsAppContactIdentity.md) |  | 
**Current** | [**WhatsAppContactIdentity**](WhatsAppContactIdentity.md) |  | 
**ContactId** | **string** | Zernio contact id matched on the new identity, null when none exists yet. | 
**ConversationId** | **string** | Zernio inbox conversation that was re-keyed, null when there was none. | 
**ChangedAt** | **DateTime** | When Meta reported the change. | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

