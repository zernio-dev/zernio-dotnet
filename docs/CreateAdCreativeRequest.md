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
**CreativeFeatures** | **Dictionary&lt;string, CreateAdCreativeRequest.InnerEnum&gt;** | Advantage+ creative enhancements: partial map of Meta creative feature keys (snake_case) to enroll status, forwarded as degrees_of_freedom_spec.creative_features_spec. Unspecified features default to OPT_OUT. | [optional] 
**MultiAdvertiser** | **string** | Meta only. Multi-advertiser ads: whether Meta may show this ad alongside other advertisers&#39; in one unit. Meta auto-enrols since Aug 2024, so send OPT_OUT to leave. It is a top-level creative field, NOT a &#x60;creativeFeatures&#x60; key — Meta rejects it there. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

