# Zernio.Model.DuplicateAdSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | 
**CampaignId** | **string** | Destination platform campaign id (defaults to the source&#39;s campaign) | [optional] 
**DeepCopy** | **bool** | Copy child ads + creatives | [optional] [default to true]
**StatusOption** | **string** |  | [optional] [default to StatusOptionEnum.PAUSED]
**StartTime** | **DateTime** | Reschedule the copy&#39;s start (ISO 8601). A value without an offset (&#x60;YYYY-MM-DD&#x60;, &#x60;YYYY-MM-DD HH:MM:SS&#x60; or &#x60;YYYY-MM-DDTHH:MM:SS&#x60;) is read in the ad account timezone. | [optional] 
**EndTime** | **DateTime** | Reschedule the copy&#39;s end, read like &#x60;startTime&#x60;; a date-only end runs to 23:59:59 local. | [optional] 
**RenameStrategy** | **string** |  | [optional] 
**RenamePrefix** | **string** |  | [optional] 
**RenameSuffix** | **string** |  | [optional] 
**SyncAfter** | **bool** |  | [optional] [default to true]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

