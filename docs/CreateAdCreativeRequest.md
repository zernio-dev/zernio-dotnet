# Zernio.Model.CreateAdCreativeRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token and Page. | 
**AdAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). | 
**Headline** | **string** |  | 
**Body** | **string** | Primary text | 
**Description** | **string** | Link description below the headline; omitted &#x3D; Meta scrapes the destination&#39;s OG description. | [optional] 
**CallToAction** | **string** | CTA type (same whitelist as POST /v1/ads/create). | [optional] [default to "LEARN_MORE"]
**LinkUrl** | **string** |  | 
**ImageUrl** | **string** | Publicly reachable image; uploaded to the account&#39;s library server-side. | [optional] 
**ImageHash** | **string** | Existing library image hash (POST /v1/ads/images or GET /v1/ads/images). | [optional] 
**CarouselCards** | [**List&lt;CreateAdCreativeRequestCarouselCardsInner&gt;**](CreateAdCreativeRequestCarouselCardsInner.md) |  | [optional] 
**UrlTags** | **string** | Appended to every outbound URL (e.g. utm_source&#x3D;fb). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

