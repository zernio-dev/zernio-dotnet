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
**BidStrategy** | **string** | Campaign bid strategy. Meta puts &#x60;bid_strategy&#x60; where the budget lives, so this applies only alongside a campaign budget (CBO). Previously settable only via &#x60;PUT /v1/ads/campaigns/{campaignId}&#x60;. | [optional] 
**BidAmount** | **decimal** | Whole currency units (USD: 5 &#x3D; $5.00). Required for LOWEST_COST_WITH_BID_CAP and COST_CAP; ignored otherwise. | [optional] 
**RoasAverageFloor** | **decimal** | Decimal ROAS multiplier (2.0 &#x3D; 2.0x). Required for LOWEST_COST_WITH_MIN_ROAS. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

