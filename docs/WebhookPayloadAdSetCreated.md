# Zernio.Model.WebhookPayloadAdSetCreated
Webhook payload for the `ad_set.created` event. Fires when an ad set is created through Zernio (API, MCP or dashboard) or detected by the sync, once per ad set, after its row is recorded so `GET /v1/ads/ad-sets/{adSetId}` finds it.  `source` is `zernio` for ad sets created through Zernio and `platform` for ad sets our sync detected, up to one sync interval later. History loaded when an account connects, and ad sets created more than 7 days ago, are never announced.  An ad set is announced at most once per 24 hours. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. | 
**Profiles** | [**List&lt;WebhookProfilesInner&gt;**](WebhookProfilesInner.md) | The profiles this event belongs to, each with the externalId you set on it (null when none is set). Use it to route the event to your tenant without storing Zernio profile ids.  Present on every event tied to a profile, absent on events that belong to none. Events spanning several profiles (a post published to accounts of different profiles) list each once.  | [optional] 
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Event** | **string** |  | 
**Account** | [**WebhookAdsAccount**](WebhookAdsAccount.md) |  | 
**AdObject** | [**WebhookPayloadAdSetCreatedAdObject**](WebhookPayloadAdSetCreatedAdObject.md) |  | 
**Source** | **string** | Where the ad set was created. &#x60;zernio&#x60; for ad sets created through Zernio, &#x60;platform&#x60; for ad sets the sync detected. | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

