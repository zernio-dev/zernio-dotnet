# Zernio.Model.ConversationAdAttribution
The ad that opened the conversation, enriched from the ads Zernio syncs for the account owner. null when the conversation did not start from a Meta referral (ad click or ig.me / m.me ref link).  Meta's referral carries the ad ID but no campaign or ad set ID. When the ad is in your synced ads (`GET /v1/ads`), `synced` is true and the ad name, campaign, ad set and ad account come from there. Otherwise `synced` is false, `name` falls back to the ad title (Instagram, Facebook) or headline (WhatsApp) Meta sent with the click, and the other fields are null.  A team member limited to some profiles, or an API key scoped to profiles, is enriched only from the ads it can list with `GET /v1/ads`; any other ad comes back `synced` false.  A non-null object with `adId` null is a referral that is not an ad click: an ig.me / m.me ref link (`name` null) or a WhatsApp click on a post (`ctwa_source_type` post, `name` is Meta's headline). Nothing is looked up in your ads for it and `synced` is false. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdId** | **string** | Meta&#39;s ad ID: &#x60;meta_ad_id&#x60; on Instagram and Facebook, &#x60;ctwa_source_id&#x60; on WhatsApp when &#x60;ctwa_source_type&#x60; is &#x60;ad&#x60;. Accepted by &#x60;GET /v1/ads/{adId}&#x60;. | 
**Name** | **string** | The synced ad&#39;s name, else the ad title or headline Meta sent. | 
**Synced** | **bool** | True when the ad was found in your synced ads. | 
**CampaignId** | **string** | Meta campaign ID. Synced ads only. | 
**CampaignName** | **string** | Campaign name. Synced ads only. | 
**AdSetId** | **string** | Meta ad set ID. Synced ads only. | 
**AdSetName** | **string** | Ad set name. Synced ads only. | 
**AdAccountId** | **string** | Meta ad account ID (act_...). Synced ads only. | 
**AdAccountName** | **string** | Ad account name. Synced ads only. | 
**PlatformPostId** | **string** | The post the ad promotes, from the synced ad or else Meta&#39;s &#x60;post_id&#x60; on the click. | 
**IsExternal** | **bool?** | True when the ad was created outside Zernio (synced from Ads Manager), false when created through Zernio, null when not synced. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

