# Zernio.Model.WebhookPayloadAdAccountStatusChanged
Webhook payload for the `ad_account.status_changed` event. Fires when an ad account Zernio already tracked moves between `active`, `restricted`, `disabled` and `closed`, as read by Zernio's ad account discovery (Meta, Google, TikTok, X). An account seen for the first time, an account not seen in the last 48 hours, or a platform status Zernio does not recognize, never fires it.  `restricted` means the account exists but cannot run ads normally until something is settled (Meta unpaid balance or risk review, TikTok limits or pending verification, X review). Each new status fires at most once per account per 24 hours. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. | 
**Profiles** | [**List&lt;WebhookProfilesInner&gt;**](WebhookProfilesInner.md) | The profiles this event belongs to, each with the externalId you set on it (null when none is set). Present on every event tied to a profile and absent on events that belong to none. Events spanning several profiles (a post published to accounts of different profiles) list each once. Use it to route the event to your tenant without storing Zernio profile ids. | [optional] 
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Event** | **string** |  | 
**Account** | [**WebhookAdsAccount**](WebhookAdsAccount.md) |  | 
**AdAccount** | [**WebhookPayloadAdAccountStatusChangedAdAccount**](WebhookPayloadAdAccountStatusChangedAdAccount.md) |  | 
**Status** | [**WebhookPayloadAdAccountStatusChangedStatus**](WebhookPayloadAdAccountStatusChangedStatus.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

