# Zernio.Model.CreateAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | 
**AdAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). | 
**Name** | **string** |  | 
**Goal** | **string** | Mapped to the ODAX objective (same mapping as POST /v1/ads/create). | 
**SpecialAdCategories** | **List&lt;CreateAdCampaignRequest.SpecialAdCategoriesEnum&gt;** |  | [optional] 
**BudgetAmount** | **decimal** | Campaign-level (CBO) budget in whole currency units. Requires budgetType. | [optional] 
**BudgetType** | **string** |  | [optional] 
**Status** | **string** |  | [optional] [default to StatusEnum.PAUSED]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

