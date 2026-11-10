# Zernio.Model.WebhookPayloadEmailSent
Webhook payload for email.sent.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Profiles** | [**List&lt;WebhookProfilesInner&gt;**](WebhookProfilesInner.md) | The profiles this event belongs to, each with the externalId you set on it (null when none is set). Use it to route the event to your tenant without storing Zernio profile ids.  Present on every event tied to a profile, absent on events that belong to none. Events spanning several profiles (a post published to accounts of different profiles) list each once.  | [optional] 
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Event** | **string** |  | 
**Account** | [**WebhookPayloadCalendarEventAccount**](WebhookPayloadCalendarEventAccount.md) |  | 
**Source** | **string** |  | 
**Email** | [**WebhookPayloadEmailSentEmail**](WebhookPayloadEmailSentEmail.md) |  | 
**DraftId** | **string** | The draft it was sent from (&#x60;source: draft&#x60;, or a scheduled draft). | [optional] 
**ScheduleId** | **string** | The scheduled send (&#x60;source: scheduled&#x60;). | [optional] 
**ReplyToMessageId** | **string** |  | [optional] 
**ForwardedFrom** | **string** |  | [optional] 
**Timestamp** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

