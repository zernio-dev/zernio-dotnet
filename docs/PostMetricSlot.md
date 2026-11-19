# Zernio.Model.PostMetricSlot

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DayOfWeek** | **int** | UTC weekday the posts were published, 1 (Monday) to 7. | 
**Hour** | **int** | UTC hour the posts were published, 0 to 23. | 
**PostCount** | **int** | Posts published in the slot that have been synced at least once. | 
**Metrics** | **Dictionary&lt;string, decimal?&gt;** | Each metric asked, summed over each post&#39;s latest snapshot; engagementRate pools them. null when no platform of the slot reports it. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

