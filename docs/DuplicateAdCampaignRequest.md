# Zernio.Model.DuplicateAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | 
**DeepCopy** | **bool** | Copy child ad sets + ads + creatives + targeting | [optional] [default to true]
**StatusOption** | **string** | ACTIVE &#x3D; launch the clone immediately (spends the moment LinkedIn approves it). PAUSED &#x3D; clone stays DRAFT, safe default. INHERITED_FROM_SOURCE &#x3D; mirror each entity&#39;s source status per-entity. Duplicating an ACTIVE campaign this way starts a second front of spend.  | [optional] [default to StatusOptionEnum.PAUSED]
**StartTime** | **DateTime** | Reschedule the copied hierarchy&#39;s start time | [optional] 
**EndTime** | **DateTime** |  | [optional] 
**RenameStrategy** | **string** |  | [optional] 
**RenamePrefix** | **string** |  | [optional] 
**RenameSuffix** | **string** |  | [optional] 
**SyncAfter** | **bool** | Trigger ads discovery on the owning account after the copy succeeds | [optional] [default to true]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

