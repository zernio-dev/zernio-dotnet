# Zernio.Model.WebhookPayloadAutomationAlert
Webhook payload for `automation.alert.opened`, `automation.alert.escalated` and `automation.alert.resolved`: an alert episode of an automation with a lifecycle (an ad rule's `lifecycle`).  Sent as soon as the check records the change; a resolve that a pause or reactivation causes is sent once it applies. A streak that never opened sends nothing. Alerts closed outside a check (the rule turned off, deleted or its `lifecycle` removed between checks, or the daily cleanup) are not announced. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. | 
**Profiles** | [**List&lt;WebhookProfilesInner&gt;**](WebhookProfilesInner.md) | The profiles this event belongs to, each with the externalId you set on it (null when none is set). Use it to route the event to your tenant without storing Zernio profile ids.  Present on every event tied to a profile, absent on events that belong to none. Events spanning several profiles (a post published to accounts of different profiles) list each once.  | [optional] 
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Event** | **string** |  | 
**Automation** | [**WebhookAutomationRef**](WebhookAutomationRef.md) |  | 
**AccountId** | **string** | The connected account the automation acts on. | 
**CheckId** | **string** | The check that moved the alert. | 
**Alert** | [**WebhookPayloadAutomationAlertAlert**](WebhookPayloadAutomationAlertAlert.md) |  | 
**Timestamp** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

