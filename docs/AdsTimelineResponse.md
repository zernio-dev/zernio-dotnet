# Zernio.Model.AdsTimelineResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BackfillPending** | **bool** | Meta only. Present and true while historical data is being backfilled. | [optional] 
**PreviousRows** | **List&lt;Dictionary&lt;string, Object&gt;&gt;** | Only with &#x60;compare&#x3D;previous&#x60;. The daily rows of &#x60;previousRange&#x60;, in the same shape as &#x60;rows&#x60;. | [optional] 
**PreviousRange** | [**AdsTimelineResponsePreviousRange**](AdsTimelineResponsePreviousRange.md) |  | [optional] 
**Rows** | [**List&lt;AdsTimelineResponseRowsInner&gt;**](AdsTimelineResponseRowsInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

