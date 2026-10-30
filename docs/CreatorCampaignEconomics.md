# Zernio.Model.CreatorCampaignEconomics
How the campaign pays, picked by `type`. Amounts are USD cents.  Every type carries `budgetCents`, the most the campaign can pay out in total. Once earnings reach it, the campaign stops accruing and `creator_campaign.budget_exhausted` fires.  - `cpm`: `ratePer1kCents` per 1,000 of the counted `metric` (views by default), earned once a post reaches `minViewsToEarn` of it, capped per post by `maxPayoutPerClipCents`. - `per_post`: `perApprovedPostCents` for each approved post, at most `maxPostsPerParticipant` per participant. - `pool`: `budgetCents` is split at close among approved posts by eligible views; a post needs `minViewsToQualify` views to share. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Metric** | **string** | What the rate pays on. &#x60;engagements&#x60; counts the &#x60;engagementTypes&#x60; as each platform reports them, and &#x60;minViewsToEarn&#x60; then applies to engagements. Fixed once the campaign leaves draft. | [optional] [default to MetricEnum.Views]
**EngagementTypes** | **List&lt;CreatorCampaignEconomics.EngagementTypesEnum&gt;** | With &#x60;metric: engagements&#x60;, the engagements that count. Missing means all four, and sending it on a views campaign answers 400. YouTube reports likes and comments only, Facebook and Threads have no saves, and Pinterest reports saves only. | [optional] 
**RatePer1kCents** | **int** |  | 
**MinViewsToEarn** | **int** | The count a post must reach before it earns, in the campaign metric (views or engagements). | 
**MaxPayoutPerClipCents** | **int** |  | [optional] 
**BudgetCents** | **int** |  | 
**PerApprovedPostCents** | **int** |  | 
**MaxPostsPerParticipant** | **int** |  | [optional] 
**MinViewsToQualify** | **int** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

