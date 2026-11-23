# Zernio.Model.AdSetMetricRow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | 
**AdAccountId** | **string** |  | 
**CampaignId** | **string** |  | 
**AdSetId** | **string** |  | 
**Name** | **string** | The ad set name. null before its first sync. | 
**Currency** | **string** | The ad account currency every money metric of this ad set is in. Ad sets of different ad accounts are never summed together. | 
**Metrics** | [**AdMetrics**](AdMetrics.md) | Only the asked metrics, summed over every ad of the ad set with rates recomputed from the sums. reach is deduplicated across the range for Meta and TikTok when the platform returns it. | 
**Daily** | [**List&lt;CampaignMetricRowDailyInner&gt;**](CampaignMetricRowDailyInner.md) | With granularity&#x3D;day, one point per day with delivery, each carrying date and the asked metrics. | [optional] 
**LastSyncedAt** | **string** | When the newest daily row of the ad set was synced. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

