# Zernio.Model.WebhookPayloadCampaignBudgetDepleted
Webhook payload for the `campaign.budget.depleted` event. Fires when a campaign Zernio already tracked stops delivering because its budget ran out. TikTok only: it is the one network that reports an exhausted budget on the ad. Meta and Google keep such ads `ACTIVE`, so they never fire it.  Detected by Zernio's own ad sync. Each campaign fires at most once per 6 hours, so a daily budget that runs out again the next day is announced again. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. | 
**Profiles** | [**List&lt;WebhookProfilesInner&gt;**](WebhookProfilesInner.md) | The profiles this event belongs to, each with the externalId you set on it (null when none is set). Use it to route the event to your tenant without storing Zernio profile ids.  Present on every event tied to a profile, absent on events that belong to none. Events spanning several profiles (a post published to accounts of different profiles) list each once.  | [optional] 
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Event** | **string** |  | 
**Account** | [**WebhookAdsAccount**](WebhookAdsAccount.md) |  | 
**AdObject** | [**WebhookPayloadCampaignBudgetDepletedAdObject**](WebhookPayloadCampaignBudgetDepletedAdObject.md) |  | 
**Budget** | [**WebhookPayloadCampaignBudgetDepletedBudget**](WebhookPayloadCampaignBudgetDepletedBudget.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

