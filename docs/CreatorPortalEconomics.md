# Zernio.Model.CreatorPortalEconomics
How the campaign pays, without its budget. Amounts in cents. A pool campaign shows the pool size as `poolCents`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Metric** | **string** | What the rate pays on. Missing means views. | [optional] 
**EngagementTypes** | **List&lt;CreatorPortalEconomics.EngagementTypesEnum&gt;** | The engagements that count. Missing means all four. | [optional] 
**RatePer1kCents** | **int** |  | 
**MinViewsToEarn** | **int** |  | 
**MaxPayoutPerClipCents** | **int** |  | [optional] 
**PerApprovedPostCents** | **int** |  | 
**MaxPostsPerParticipant** | **int** |  | [optional] 
**PoolCents** | **int** |  | 
**MinViewsToQualify** | **int** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

