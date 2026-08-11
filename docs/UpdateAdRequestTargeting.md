# Zernio.Model.UpdateAdRequestTargeting
Meta + TikTok (demographics/interests) and Google (keyword edits only). Pinterest / X / LinkedIn return 501. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Keywords** | [**List&lt;UpdateAdRequestTargetingKeywordsInner&gt;**](UpdateAdRequestTargetingKeywordsInner.md) | Google only. The FULL new set of positive keywords for the ad group; live keywords not listed are removed. Entries are strings (BROAD) or { text, matchType } with matchType exact | phrase | broad. Mirrored to GET /v1/ads/keywords immediately. | [optional] 
**NegativeKeywords** | [**List&lt;UpdateAdRequestTargetingKeywordsInner&gt;**](UpdateAdRequestTargetingKeywordsInner.md) | Google only. Same declarative contract as keywords, for the ad group&#39;s negative keywords. | [optional] 
**AgeMin** | **int** |  | [optional] 
**AgeMax** | **int** |  | [optional] 
**Countries** | **List&lt;string&gt;** |  | [optional] 
**Interests** | [**List&lt;UpdateAdRequestTargetingInterestsInner&gt;**](UpdateAdRequestTargetingInterestsInner.md) | Interest objects from /v1/ads/interests. Each must include id and name. | [optional] 
**AdvantageAudience** | **int** | Meta only. Omit to preserve the existing setting on update. 0 &#x3D; disabled, 1 &#x3D; enabled. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

