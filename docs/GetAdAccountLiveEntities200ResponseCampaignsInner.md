# Zernio.Model.GetAdAccountLiveEntities200ResponseCampaignsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PlatformCampaignId** | **string** |  | [optional] 
**CampaignName** | **string** |  | [optional] 
**PlatformCampaignStatus** | **string** | Meta &#x60;effective_status&#x60;, for example ACTIVE, PAUSED, WITH_ISSUES. | [optional] 
**ConfiguredStatus** | **string** | Meta &#x60;status&#x60;: the campaign&#39;s own switch (ACTIVE, PAUSED, DELETED, ARCHIVED). | [optional] 
**Status** | **string** | Zernio&#39;s normalized status (active, paused, ...), derived from &#x60;platformCampaignStatus&#x60;. | [optional] 
**Budget** | [**GetAdAccountLiveEntities200ResponseCampaignsInnerBudget**](GetAdAccountLiveEntities200ResponseCampaignsInnerBudget.md) |  | [optional] 
**DailyBudget** | **decimal?** | Meta &#x60;daily_budget&#x60; in whole units of &#x60;currency&#x60;. | [optional] 
**LifetimeBudget** | **decimal?** | Meta &#x60;lifetime_budget&#x60; in whole units of &#x60;currency&#x60;. | [optional] 
**BudgetRemaining** | **decimal?** | Meta &#x60;budget_remaining&#x60; in whole units of &#x60;currency&#x60;. Null when the campaign has no budget of its own. | [optional] 
**SpendCap** | **decimal?** | Campaign spending limit (Meta &#x60;spend_cap&#x60;) in whole units of &#x60;currency&#x60;. Null when none is set. | [optional] 
**BidStrategy** | **string** | Meta &#x60;bid_strategy&#x60;, set on campaigns with a campaign budget. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

