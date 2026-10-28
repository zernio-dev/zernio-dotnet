# Zernio.Model.CreatorPortalCampaign
The campaign as a creator sees it: terms, never the budget.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The campaign id, as in a link-recovery URL. | 
**Name** | **string** |  | 
**BrandName** | **string** |  | 
**LogoUrl** | **string** |  | 
**Theme** | **Object** | Same keys as the &#x60;welcomeTheme&#x60; parameter of &#x60;GET /v1/connect/{platform}&#x60;. | 
**Status** | **string** |  | 
**Platforms** | **List&lt;string&gt;** |  | 
**ContentRules** | **string** |  | 
**StartsAt** | **DateTime?** |  | 
**EndsAt** | **DateTime?** |  | 
**Currency** | **string** |  | 
**Economics** | [**CreatorPortalEconomics**](CreatorPortalEconomics.md) |  | 
**MaxPostAgeMinutes** | **int** | A post must be submitted within this many minutes of publishing. | 
**HoldDays** | **int** | Days approved earnings stay owed before they become payable. | 
**TrackingDays** | **int** | Days each submitted post is tracked for views. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

