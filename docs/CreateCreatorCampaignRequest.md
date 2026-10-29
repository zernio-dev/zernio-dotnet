# Zernio.Model.CreateCreatorCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** | Profile the campaign lives in. Creator accounts connect into the same workspace. | 
**Name** | **string** |  | 
**BrandName** | **string** |  | 
**Economics** | [**CreatorCampaignEconomics**](CreatorCampaignEconomics.md) |  | 
**Caps** | [**CreatorCampaignCaps**](CreatorCampaignCaps.md) | Omitted, the campaign starts with authenticityThreshold 40 and no other caps. | [optional] 
**Platforms** | **List&lt;CreateCreatorCampaignRequest.PlatformsEnum&gt;** | Platforms creators may post on. At least one is needed to activate. &#x60;twitter&#x60; (X) needs usage-based billing: X reads are billed at cost, up to &#x60;caps.maxXReadSpendCents&#x60;, and X views are the post&#39;s impressions. &#x60;facebook&#x60; takes Page reels and videos only. | [optional] 
**ContentRules** | **string** |  | [optional] 
**StartsAt** | **DateTime?** |  | [optional] 
**EndsAt** | **DateTime?** |  | [optional] 
**TrackingDays** | **int** |  | [optional] [default to 30]
**HoldDays** | **int** |  | [optional] [default to 10]
**MaxPostAgeMinutes** | **int?** | Optional maximum age in minutes of a post when it is submitted. Null or omitted (the default) accepts any age. Posts published before the campaign started are always refused. | [optional] 
**Settlement** | **string** |  | [optional] [default to SettlementEnum.None]
**Branding** | [**CreatorCampaignBranding**](CreatorCampaignBranding.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

