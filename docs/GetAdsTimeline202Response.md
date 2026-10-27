# Zernio.Model.GetAdsTimeline202Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BackfillPending** | **bool** | Always true on this response. Part of the requested range is still being backfilled; retry until the request returns 200. | 
**PreviousRows** | **List&lt;Dictionary&lt;string, Object&gt;&gt;** | Only with &#x60;compare&#x3D;previous&#x60;. The daily rows of &#x60;previousRange&#x60;, in the same shape as &#x60;rows&#x60;. | [optional] 
**PreviousRange** | [**AdsTimelineResponsePreviousRange**](AdsTimelineResponsePreviousRange.md) |  | [optional] 
**Rows** | [**List&lt;AdsTimelineResponseRowsInner&gt;**](AdsTimelineResponseRowsInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

