# Zernio.Model.WebhookPayloadMessageMetadataReferral
Ad-click attribution forwarded verbatim from Meta. Populated only on the FIRST inbound message after the click; absent on subsequent messages of the same conversation.  The populated subset identifies the source platform:   - `ctwa_clid` and `source_*` fields: WhatsApp CTWA     (Click-to-WhatsApp). Attribution window is 7 days from click.     Forward to Meta Conversions API for Business Messaging replay.   - `ad_id` and `ads_context_data`: Facebook Messenger CTM     (Click-to-Message) or Instagram CTD (Click-to-Direct). Use     `ad_id` to attribute the conversation to a specific ad. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CtwaClid** | **string** | Meta&#39;s GCLID-equivalent click identifier. | [optional] 
**SourceId** | **string** |  | [optional] 
**SourceType** | **string** |  | [optional] 
**SourceUrl** | **string** |  | [optional] 
**Headline** | **string** |  | [optional] 
**Body** | **string** |  | [optional] 
**MediaType** | **string** |  | [optional] 
**ImageUrl** | **string** |  | [optional] 
**VideoUrl** | **string** |  | [optional] 
**ThumbnailUrl** | **string** |  | [optional] 
**AdId** | **string** | Facebook Messenger CTM / Instagram CTD only. The Meta ad ID the user clicked to start the conversation.  | [optional] 
**Ref** | **string** | Optional &#x60;ref&#x60; parameter passed through from the Meta ad creative. Facebook Messenger CTM / Instagram CTD only.  | [optional] 
**Source** | **string** | Meta-supplied source identifier (e.g. &#x60;ADS&#x60;). Facebook Messenger CTM / Instagram CTD only.  | [optional] 
**Type** | **string** | Meta-supplied referral type (e.g. &#x60;OPEN_THREAD&#x60;). Facebook Messenger CTM / Instagram CTD only.  | [optional] 
**AdsContextData** | [**WebhookPayloadMessageMetadataReferralAdsContextData**](WebhookPayloadMessageMetadataReferralAdsContextData.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

