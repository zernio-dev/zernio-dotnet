# Zernio.Model.GetAdTree202Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Campaigns** | [**List&lt;AdTreeCampaign&gt;**](AdTreeCampaign.md) |  | [optional] 
**Pagination** | [**Pagination**](Pagination.md) |  | [optional] 
**SyncedAt** | **DateTime** | When the most recently synced ad on this page was last read from the platform. Null before the first sync. | [optional] 
**PreviousRange** | [**AdTreeResponsePreviousRange**](AdTreeResponsePreviousRange.md) |  | [optional] 
**BackfillPending** | **bool** | Always true on this response. Part of the requested range is still being backfilled; retry until the request returns 200. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

