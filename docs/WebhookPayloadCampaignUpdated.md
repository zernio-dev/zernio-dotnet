# Zernio.Model.WebhookPayloadCampaignUpdated
Webhook payload for the `campaign.updated` event. Fires when a campaign is edited through Zernio (API, MCP or dashboard), after the platform and Zernio both accepted the edit, once per user who can see the campaign. It also fires when the sync detects an edit made outside Zernio.  `source` is `zernio` for edits through Zernio, `platform` for edits the sync detected outside Zernio, up to one sync interval late, sent only to the user whose sync saw it.  From the sync, `changes` covers only `name`, `status` and `schedule` (schedule only on Google, LinkedIn, Pinterest and OpenAI Ads). Budget edits made outside Zernio are not announced. Never for history loaded when an account connects. An ad rule that changes a campaign arrives as `ad_rule.triggered`.  Ad set edits and Google sub-resource edits (ad schedule, targeting, negative keywords, conversion goals, assets, asset groups, listing group filters) are not announced.  `changes` names the edited fields and never their values: read the campaign with `GET /v1/ads/campaigns/{campaignId}` for the current state. Ignore values you do not know, new ones can be added.  Events are not deduplicated: every edit is announced. Use the event `id` to drop repeats. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. | 
**Profiles** | [**List&lt;WebhookProfilesInner&gt;**](WebhookProfilesInner.md) | The profiles this event belongs to, each with the externalId you set on it (null when none is set). Use it to route the event to your tenant without storing Zernio profile ids.  Present on every event tied to a profile, absent on events that belong to none. Events spanning several profiles (a post published to accounts of different profiles) list each once.  | [optional] 
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Event** | **string** |  | 
**Account** | [**WebhookAdsAccount**](WebhookAdsAccount.md) |  | 
**AdObject** | [**WebhookPayloadCampaignCreatedAdObject**](WebhookPayloadCampaignCreatedAdObject.md) |  | 
**Changes** | **List&lt;WebhookPayloadCampaignUpdated.ChangesEnum&gt;** | Fields edited by this request. &#x60;status&#x60; is the campaign&#39;s own on/off switch. Ignore values you do not know. | 
**Source** | **string** | Where the edit was made. &#x60;zernio&#x60; for edits through Zernio, &#x60;platform&#x60; for edits the sync detected outside Zernio. | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

