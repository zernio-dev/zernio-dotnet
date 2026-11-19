# Zernio.Model.PostMetricChange

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | 
**ProfileId** | **string** |  | 
**Platform** | **string** |  | 
**PlatformPostId** | **string** |  | 
**PublishedAt** | **string** |  | 
**SyncedAt** | **string** | When the account&#39;s sync cycle that read these numbers started. Not an order: resume with the cursor only. | 
**Deleted** | **bool** | True when the post was removed from the platform. | 
**Metrics** | **Dictionary&lt;string, decimal?&gt;** | Each metric asked, as the platform reported it in this change; null when the post&#39;s platform does not report it. | 
**Breakdowns** | [**Dictionary&lt;string, PostMetricRowBreakdownsValue&gt;**](PostMetricRowBreakdownsValue.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

