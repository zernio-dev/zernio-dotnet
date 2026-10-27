# Zernio.Model.AdTreeResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Campaigns** | [**List&lt;AdTreeCampaign&gt;**](AdTreeCampaign.md) |  | [optional] 
**Pagination** | [**Pagination**](Pagination.md) |  | [optional] 
**SyncedAt** | **DateTime?** | When the most recently synced ad on this page was last read from the platform. Null before the first sync. | [optional] 
**PreviousRange** | [**AdTreeResponsePreviousRange**](AdTreeResponsePreviousRange.md) |  | [optional] 
**BackfillPending** | **bool** | Meta only. Present and true while historical data is being backfilled. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

