# Zernio.Model.CreatorCampaignEconomics
How the campaign pays, picked by `type`. Amounts are USD cents. Every type carries `budgetCents`, the most the campaign can pay out in total; once earnings reach it the campaign stops accruing and `creator_campaign.budget_exhausted` fires. - `cpm`: `ratePer1kCents` per 1,000 eligible views, earned from `minViewsToEarn` views on, capped per post by `maxPayoutPerClipCents`. - `per_post`: `perApprovedPostCents` for each approved post, at most `maxPostsPerParticipant` per participant. - `pool`: `budgetCents` is split at close among approved posts by eligible views; a post needs `minViewsToQualify` views to share. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**RatePer1kCents** | **int** |  | 
**MinViewsToEarn** | **int** |  | 
**MaxPayoutPerClipCents** | **int** |  | [optional] 
**BudgetCents** | **int** |  | 
**PerApprovedPostCents** | **int** |  | 
**MaxPostsPerParticipant** | **int** |  | [optional] 
**MinViewsToQualify** | **int** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

