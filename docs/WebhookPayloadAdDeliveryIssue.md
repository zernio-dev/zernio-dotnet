# Zernio.Model.WebhookPayloadAdDeliveryIssue
Webhook payload for the `ad.delivery_issue` event. Fires when an ad Zernio already tracked moves into the platform's error state: Meta `WITH_ISSUES` (payment, policy and account problems), TikTok account punishment or missing balance, LinkedIn removals, and any platform status Zernio does not recognize yet (check `issue.raw`). Ads seen for the first time by a sync never fire it.  Detected by Zernio's own ad sync, so it arrives within one sync cycle. Each ad fires at most once per 24 hours. On Meta, `ad.status_changed` with `WITH_ISSUES` can also fire for the same problem, straight from Meta's webhook. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. | 
**Profiles** | [**List&lt;WebhookProfilesInner&gt;**](WebhookProfilesInner.md) | The profiles this event belongs to, each with the externalId you set on it (null when none is set). Present on every event tied to a profile and absent on events that belong to none. Events spanning several profiles (a post published to accounts of different profiles) list each once. Use it to route the event to your tenant without storing Zernio profile ids. | [optional] 
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Event** | **string** |  | 
**Account** | [**WebhookAdsAccount**](WebhookAdsAccount.md) |  | 
**AdObject** | [**WebhookPayloadAdReviewAdObject**](WebhookPayloadAdReviewAdObject.md) |  | 
**Issue** | [**WebhookPayloadAdDeliveryIssueIssue**](WebhookPayloadAdDeliveryIssueIssue.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

