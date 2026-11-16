# Zernio.Model.WebhookPayloadAccountPrivacyRequest
Webhook payload for account.privacy_request: a Shopify merchant asked to export or erase a customer's data, or the shop's data 48 hours after an uninstall.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Profiles** | [**List&lt;WebhookProfilesInner&gt;**](WebhookProfilesInner.md) | The profiles this event belongs to, each with the externalId you set on it (null when none is set). Use it to route the event to your tenant without storing Zernio profile ids.  Present on every event tied to a profile, absent on events that belong to none. Events spanning several profiles (a post published to accounts of different profiles) list each once.  | [optional] 
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Event** | **string** |  | 
**Account** | [**WebhookPayloadAccountPrivacyRequestAccount**](WebhookPayloadAccountPrivacyRequestAccount.md) |  | 
**PrivacyRequest** | [**WebhookPayloadAccountPrivacyRequestPrivacyRequest**](WebhookPayloadAccountPrivacyRequestPrivacyRequest.md) |  | 
**Timestamp** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

