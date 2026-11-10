# Zernio.Model.CreatorPortalEconomics
How the campaign pays, without its budget. Amounts in cents. A pool campaign shows the pool size as `poolCents`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Metric** | **string** | What the rate pays on. Missing means views. | [optional] 
**EngagementTypes** | **List&lt;CreatorPortalEconomics.EngagementTypesEnum&gt;** | The engagements that count. Missing means all four. | [optional] 
**OrganicViewsOnly** | **bool** | Only organic views count; views from ads do not. | [optional] 
**RatePer1kCents** | **int** |  | 
**MinViewsToEarn** | **int** |  | 
**MaxPayoutPerClipCents** | **int** |  | [optional] 
**PerApprovedPostCents** | **int** |  | 
**MaxPostsPerParticipant** | **int** |  | [optional] 
**PoolCents** | **int** |  | 
**MinViewsToQualify** | **int** |  | 
**Mode** | **string** |  | 
**AmountCents** | **int** |  | 
**Period** | **string** |  | 
**RequiredApprovedPosts** | **int** |  | 
**Commission** | [**CreatorCampaignCommissionTerms**](CreatorCampaignCommissionTerms.md) |  | 
**PercentOfSalesBps** | **int** | Share of the sales in basis points: 1500 is 15%. | [optional] 
**PerOrderCents** | **int** | A flat amount per credited order. | [optional] 
**Attribution** | **string** | How an order is credited: the creator&#39;s discount code, the last click on their tracking link, or both with the code winning. | [optional] [default to AttributionEnum.CodeOrLink]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

