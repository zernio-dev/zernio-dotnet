# Zernio.Model.UpdateCreatorCampaignRequest
Every field is optional; send at least one. `economics` can only change while the campaign is a draft.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | [optional] 
**BrandName** | **string** |  | [optional] 
**Platforms** | **List&lt;UpdateCreatorCampaignRequest.PlatformsEnum&gt;** |  | [optional] 
**ContentRules** | **string** |  | [optional] 
**StartsAt** | **DateTime?** |  | [optional] 
**EndsAt** | **DateTime?** |  | [optional] 
**TrackingDays** | **int** |  | [optional] 
**HoldDays** | **int** |  | [optional] 
**MaxPostAgeMinutes** | **int** |  | [optional] 
**Settlement** | **string** |  | [optional] 
**Economics** | [**CreatorCampaignEconomics**](CreatorCampaignEconomics.md) |  | [optional] 
**Caps** | [**CreatorCampaignCaps**](CreatorCampaignCaps.md) |  | [optional] 
**Branding** | [**CreatorCampaignBranding**](CreatorCampaignBranding.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

