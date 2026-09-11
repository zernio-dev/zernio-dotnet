# Zernio.Model.CreateAdCreativeRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token and Page. | 
**AdAccountId** | **string** | Platform ad account id (Meta act_&lt;n&gt;, Google customer id, LinkedIn account id, ...). | 
**Headline** | **string** |  | 
**Body** | **string** | Primary text | 
**Description** | **string** | Link description below the headline; omitted &#x3D; Meta scrapes the destination&#39;s OG description. | [optional] 
**CallToAction** | **string** | CTA type (same whitelist as POST /v1/ads/create). | [optional] [default to "LEARN_MORE"]
**LinkUrl** | **string** |  | 
**ImageUrl** | **string** | Publicly reachable image; uploaded to the account&#39;s library server-side. | [optional] 
**ImageHash** | **string** | Existing library image hash (POST /v1/ads/images or GET /v1/ads/images). | [optional] 
**CarouselCards** | [**List&lt;CreateAdCreativeRequestCarouselCardsInner&gt;**](CreateAdCreativeRequestCarouselCardsInner.md) |  | [optional] 
**UrlTags** | **string** | Appended to every outbound URL (e.g. utm_source&#x3D;fb). | [optional] 
**Promotion** | **Object** | Not supported. Meta validates creative_sourcing_spec.promotion_metadata_spec on the create call and then discards it, so a Promotion set through the Marketing API never reaches the creative. Any object is rejected with 400 invalid_field_value. Send null or omit the field, and set the Promotion on the ad in Ads Manager. Verified on 2026-09-11 across Graph v19.0 to v25.0 and every write path. | [optional] 
**CreativeFeatures** | **Dictionary&lt;string, CreateAdCreativeRequest.InnerEnum&gt;** | Meta only. Applied to each new creative, including standalone and attach shapes. With creatives[], these are defaults; an item replaces the whole feature map, including an empty map. auto_promotion_tag is an Advantage+ enhancement, not the Ads Manager Promotion setting. | [optional] 
**MultiAdvertiser** | **string** | Meta only. Multi-advertiser ads: whether Meta may show this ad alongside other advertisers&#39; in one unit. Meta auto-enrols since Aug 2024, so send OPT_OUT to leave. It is a top-level creative field, NOT a &#x60;creativeFeatures&#x60; key, and Meta rejects it there. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

