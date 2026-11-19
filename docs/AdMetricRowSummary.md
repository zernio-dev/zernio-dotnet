# Zernio.Model.AdMetricRowSummary
The ad over fromDate to toDate, money in the ad account currency.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Spend** | **decimal** |  | 
**Impressions** | **decimal** |  | 
**Reach** | **decimal** | Deduplicated across days for Meta ads when the platform returns it. | 
**Clicks** | **decimal** |  | 
**Engagement** | **decimal** |  | 
**Ctr** | **decimal** |  | 
**Cpc** | **decimal** |  | 
**Cpm** | **decimal** |  | 
**Conversions** | **decimal** |  | 
**AllConversions** | **decimal** |  | 
**CostPerConversion** | **decimal** |  | 
**Actions** | **Dictionary&lt;string, decimal&gt;** |  | 
**ActionValues** | **Dictionary&lt;string, decimal&gt;** |  | 
**PurchaseValue** | **decimal** |  | 
**Roas** | **decimal** |  | 
**CostPerAction** | **Dictionary&lt;string, decimal&gt;** |  | 
**OutboundClicks** | **decimal** |  | 
**OutboundClicksCtr** | **decimal** |  | 
**InlineLinkClicks** | **decimal** |  | 
**InlineLinkClickCtr** | **decimal** |  | 
**UniqueClicks** | **decimal** |  | 
**UniqueCtr** | **decimal** |  | 
**Funnel** | **Dictionary&lt;string, decimal&gt;** |  | 
**EngagementBreakdown** | **Dictionary&lt;string, decimal&gt;** |  | 
**VideoPlayActions** | **decimal** |  | 
**Video30SecWatchedActions** | **decimal** |  | 
**VideoThruplayWatchedActions** | **decimal** |  | 
**VideoP25WatchedActions** | **decimal** |  | 
**VideoP50WatchedActions** | **decimal** |  | 
**VideoP75WatchedActions** | **decimal** |  | 
**VideoP95WatchedActions** | **decimal** |  | 
**VideoP100WatchedActions** | **decimal** |  | 
**VideoAvgTimeWatchedActions** | **decimal** |  | 
**Video2SecWatchedActions** | **decimal** |  | 
**Video6SecWatchedActions** | **decimal** |  | 
**Video6SecFocusedViews** | **decimal** |  | 
**CostPerThruplay** | **decimal** |  | 
**LastSyncedAt** | **string** |  | 
**QualityRanking** | **string** |  | [optional] 
**EngagementRateRanking** | **string** |  | [optional] 
**ConversionRateRanking** | **string** |  | [optional] 
**VideoTotalWatchTime** | **decimal** | Reading one ad: average watch time times plays, summed over the days. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

