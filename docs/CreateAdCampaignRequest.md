# Zernio.Model.CreateAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id (posting or ads variant); its platform decides where the campaign is created. | 
**AdAccountId** | **string** | Platform ad account id (Meta act_&lt;n&gt;, Google customer id, LinkedIn account id, ...). | 
**Name** | **string** |  | 
**Goal** | **string** | Mapped to the ODAX objective (same mapping as POST /v1/ads/create). | 
**SpecialAdCategories** | **List&lt;CreateAdCampaignRequest.SpecialAdCategoriesEnum&gt;** |  | [optional] 
**BudgetAmount** | **decimal** | Campaign-level (CBO) budget in WHOLE currency units (USD: 50 &#x3D; $50.00), NOT cents — Meta&#39;s own Marketing API takes this same number in minor units, so it is an easy and expensive mix-up. Requires budgetType. | [optional] 
**BudgetType** | **string** |  | [optional] 
**Status** | **string** |  | [optional] [default to StatusEnum.PAUSED]
**BidStrategy** | **string** | Campaign bid strategy. Meta stores &#x60;bid_strategy&#x60; alongside the budget, so this REQUIRES &#x60;budgetAmount&#x60; + &#x60;budgetType&#x60; on the same request; sending it without a campaign budget is a 400. A campaign carrying a strategy without its &#x60;bid_amount&#x60; makes every ad set created under it fail with an error that names the ad set (code 100, subcode 1815857), so the bad state is rejected up front rather than accepted. To bid at ad-set level, set the strategy there instead. | [optional] 
**BidAmount** | **decimal** | Whole currency units (USD: 5 &#x3D; $5.00). Required for LOWEST_COST_WITH_BID_CAP and COST_CAP; ignored otherwise. Validated here but NOT stored by Meta: the campaign object has no bid_amount field, only bid_strategy lives on it. The amount takes effect once an ad set joins this campaign (existingCampaignId on POST /v1/ads/create) and supplies its own bidAmount there. | [optional] 
**RoasAverageFloor** | **decimal** | Decimal ROAS multiplier (2.0 &#x3D; 2.0x). Required for LOWEST_COST_WITH_MIN_ROAS. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

