# Zernio.Model.WebhookPayloadAdRuleTriggered
Webhook payload for the `ad_rule.triggered` event.  Fires when a scheduled run of a rule with a `notify` action finds campaigns or ad sets that meet every condition of the rule. Each object is announced at most once per rule cooldown, so `objects` lists only the objects the run acted on, never the ones still in cooldown. A run where every matching object is still in cooldown sends nothing. An object whose action failed gets no cooldown: the next run retries it and reports it again. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. | 
**Profiles** | [**List&lt;WebhookProfilesInner&gt;**](WebhookProfilesInner.md) | The profiles this event belongs to, each with the externalId you set on it (null when none is set). Present on every event tied to a profile and absent on events that belong to none. Events spanning several profiles (a post published to accounts of different profiles) list each once. Use it to route the event to your tenant without storing Zernio profile ids. | [optional] 
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Event** | **string** |  | 
**Account** | [**WebhookAdsAccount**](WebhookAdsAccount.md) |  | 
**Rule** | [**WebhookPayloadAdRuleTriggeredRule**](WebhookPayloadAdRuleTriggeredRule.md) |  | 
**Run** | [**WebhookPayloadAdRuleTriggeredRun**](WebhookPayloadAdRuleTriggeredRun.md) |  | 
**Objects** | [**List&lt;WebhookPayloadAdRuleTriggeredObjectsInner&gt;**](WebhookPayloadAdRuleTriggeredObjectsInner.md) | The campaigns or ad sets this run acted on, at the rule&#39;s &#x60;level&#x60;, including those whose action failed. Objects still in cooldown are left out. | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

