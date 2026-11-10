# Zernio.Model.CreatorCampaignEconomics
How the campaign pays, picked by `type`. Amounts are USD cents.  Every type carries `budgetCents`, the most the campaign can pay out in total. Once earnings reach it, the campaign stops accruing and `creator_campaign.budget_exhausted` fires.  - `cpm`: `ratePer1kCents` per 1,000 of the counted `metric` (views by default), earned once a post reaches `minViewsToEarn` of it, capped per post by `maxPayoutPerClipCents`. - `per_post`: `perApprovedPostCents` for each approved post, at most `maxPostsPerParticipant` per participant. - `pool`: `budgetCents` is split at close among approved posts by eligible views; a post needs `minViewsToQualify` views to share. - `ad_performance`: pays on the results of the ads that run each post (see `GET /v1/creator-campaigns/{campaignId}/ad-results`), counted once a day through the previous UTC day. Only Instagram, Facebook and TikTok posts. - `retainer`: `amountCents` per `period` once the creator has `requiredApprovedPosts` approved posts in it. `mode: smart` tops the period's commission up to `amountCents`. - `commission`: a share of the sales of the linked store (`storeAccountId`) credited to each creator by their discount code or tracking link. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Metric** | **string** |  | 
**EngagementTypes** | **List&lt;CreatorCampaignEconomics.EngagementTypesEnum&gt;** | With &#x60;metric: engagements&#x60;, the engagements that count. Missing means all four, and sending it on a views campaign answers 400. YouTube reports likes and comments only, Facebook and Threads have no saves, and Pinterest reports saves only. | [optional] 
**OrganicViewsOnly** | **bool** | Count only organic views: views from ads the creator ran do not earn. Every campaign platform must be YouTube or X, which report ad views per post, or the request answers 400. A post earns nothing until its ad views were first read. | [optional] [default to false]
**RatePer1kCents** | **int** |  | 
**MinViewsToEarn** | **int** | The count a post must reach before it earns, in the campaign metric (views or engagements). | 
**MaxPayoutPerClipCents** | **int** |  | [optional] 
**BudgetCents** | **int** |  | 
**PerApprovedPostCents** | **int** |  | 
**MaxPostsPerParticipant** | **int** |  | [optional] 
**MinViewsToQualify** | **int** |  | 
**RateBps** | **int** | Basis points of the spend or purchase value: 1000 is 10%. | [optional] 
**CentsPerUnit** | **int** | Cents per purchase or click, or per 1,000 impressions. | [optional] 
**MaxPayoutPerPostCents** | **int** |  | [optional] 
**Mode** | **string** | &#x60;standard&#x60; pays &#x60;amountCents&#x60; per period. &#x60;smart&#x60; guarantees it: the commission the creator earned in the period is topped up to &#x60;amountCents&#x60;. Smart needs &#x60;commission&#x60; and a linked store. | [optional] [default to ModeEnum.Standard]
**AmountCents** | **int** |  | 
**Period** | **string** | Weeks start Monday 00:00 UTC, months on the 1st. A period is paid within a day after it ends. A standard &#x60;once&#x60; retainer pays as soon as the posts are approved; a smart one when the campaign ends. | 
**RequiredApprovedPosts** | **int** | Posts approved within the period that it needs. 0 pays without posts. | 
**Commission** | [**CreatorCampaignCommissionTerms**](CreatorCampaignCommissionTerms.md) |  | [optional] 
**PercentOfSalesBps** | **int** | Share of the sales in basis points: 1500 is 15%. | [optional] 
**PerOrderCents** | **int** | A flat amount per credited order. | [optional] 
**Attribution** | **string** | How an order is credited: the creator&#39;s discount code, the last click on their tracking link, or both with the code winning. | [optional] [default to AttributionEnum.CodeOrLink]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

