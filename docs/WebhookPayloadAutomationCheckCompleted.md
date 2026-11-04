# Zernio.Model.WebhookPayloadAutomationCheckCompleted
Webhook payload for the `automation.check.completed` event: one scheduled check of an automation finished.  It fires once per check, whatever the outcome, including checks where nothing matched. Ad rules are the first automations on the engine; `automation.kind` names the product. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. | 
**Profiles** | [**List&lt;WebhookProfilesInner&gt;**](WebhookProfilesInner.md) | The profiles this event belongs to, each with the externalId you set on it (null when none is set). Use it to route the event to your tenant without storing Zernio profile ids.  Present on every event tied to a profile, absent on events that belong to none. Events spanning several profiles (a post published to accounts of different profiles) list each once.  | [optional] 
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Event** | **string** |  | 
**Automation** | [**WebhookAutomationRef**](WebhookAutomationRef.md) |  | 
**AccountId** | **string** | The connected account the automation acts on. | 
**Check** | [**WebhookPayloadAutomationCheckCompletedCheck**](WebhookPayloadAutomationCheckCompletedCheck.md) |  | 
**Timestamp** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

