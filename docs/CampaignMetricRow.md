# Zernio.Model.CampaignMetricRow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | 
**AdAccountId** | **string** |  | 
**CampaignId** | **string** |  | 
**Results** | **Dictionary&lt;string, decimal&gt;** | Without metrics, each uploaded result metric summed over the range, by metric key. | [optional] 
**Name** | **string** | With metrics, the campaign name. null before its first sync. | [optional] 
**Currency** | **string** | With metrics, the ad account currency every money metric of this campaign is in. Campaigns of different ad accounts are never summed together. | [optional] 
**Metrics** | [**AdMetrics**](AdMetrics.md) | With metrics, only the asked metrics, summed over every ad of the campaign with rates recomputed from the sums. reach is deduplicated across the range for Meta and TikTok when the platform returns it. | [optional] 
**Daily** | [**List&lt;CampaignMetricRowDailyInner&gt;**](CampaignMetricRowDailyInner.md) | With granularity&#x3D;day, one point per day with delivery, each carrying date and the asked metrics. | [optional] 
**LastSyncedAt** | **string** | With metrics, when the newest daily row of the campaign was synced. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

