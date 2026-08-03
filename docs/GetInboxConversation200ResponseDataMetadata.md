# Zernio.Model.GetInboxConversation200ResponseDataMetadata
Ad-click attribution for a conversation that started from a Meta ad. Absent when the conversation did not originate from an ad click.  Captured once, on the first inbound message after the click, and never overwritten. If the same person later clicks a different ad, the original values are kept. Meta only sends the referral on that first message.  This operation currently returns only the `meta_ad_*` family, which covers Instagram Click-to-Direct and Facebook Messenger Click-to-Message. WhatsApp Click-to-WhatsApp attribution (the `ctwa_*` keys, where the ad ID is `ctwa_source_id`) is returned by `GET /v1/inbox/conversations` instead.  Every key is optional and only the keys Meta supplied are returned, so read defensively. Meta does not send a campaign or ad set ID, so none is exposed here. More keys may be added over time. Treat any key you do not recognise as an opaque string.  Key names differ from the `message.received` webhook on purpose. The webhook forwards Meta's referral verbatim (`ad_id`, `source`, `type`) while the stored conversation record uses the prefixed names below. Renaming either side would break existing integrations, so both spellings are kept. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MetaAdId** | **string** | The Meta ad ID the user clicked. Always present when a referral was captured. | [optional] 
**MetaAdSource** | **string** | Meta-supplied source identifier, for example ADS. | [optional] 
**MetaAdType** | **string** | Meta-supplied referral type, for example OPEN_THREAD. | [optional] 
**MetaAdRef** | **string** | The ref parameter passed through from the ad creative. | [optional] 
**MetaAdTitle** | **string** | Title of the ad creative at click time. | [optional] 
**MetaAdPhotoUrl** | **string** | Image of the ad creative at click time. | [optional] 
**MetaAdVideoUrl** | **string** | Video of the ad creative at click time. | [optional] 
**MetaAdPostId** | **string** | The organic post the ad promoted, when the ad was a boosted post. | [optional] 
**MetaAdProductId** | **string** | The catalogue product the user clicked, for product ads. | [optional] 
**MetaAdFlowId** | **string** | The Meta flow the ad launched, for flow ads. | [optional] 
**MetaAdCapturedAt** | **DateTime** | When Zernio stored this referral. Always present when a referral was captured. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

