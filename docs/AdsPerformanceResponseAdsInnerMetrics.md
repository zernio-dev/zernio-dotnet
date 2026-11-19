# Zernio.Model.AdsPerformanceResponseAdsInnerMetrics

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Spend** | **decimal** | In the ad&#39;s currency. | [optional] 
**Impressions** | **int** |  | [optional] 
**Reach** | **int** | People who saw the ad. De-duplicated over the range on Meta and TikTok when the platform returns it; elsewhere the sum of each day&#39;s reach, which counts a person once per day. | [optional] 
**Frequency** | **decimal** | Average times each person saw the ad: &#x60;impressions / reach&#x60;. 0 when the platform reports no reach. | [optional] 
**Clicks** | **int** |  | [optional] 
**Ctr** | **decimal** | Percent. | [optional] 
**Conversions** | **decimal** | Results over the range (see AdMetrics.conversions). | [optional] 
**CostPerConversion** | **decimal** |  | [optional] 
**PurchaseValue** | **decimal** |  | [optional] 
**Roas** | **decimal** |  | [optional] 
**ConversionsByType** | **Dictionary&lt;string, decimal&gt;** | &#x60;conversions&#x60; split by what was counted (Meta action_type or Google conversion action name). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

