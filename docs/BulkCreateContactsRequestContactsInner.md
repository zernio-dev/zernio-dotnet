# Zernio.Model.BulkCreateContactsRequestContactsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**PlatformIdentifier** | **string** | Required when the top-level accountId is set (channel mode). A row missing it in that mode is rejected individually and reported in errors[], not a 400 for the whole import. | [optional] 
**DisplayIdentifier** | **string** |  | [optional] 
**Email** | **string** |  | [optional] 
**Company** | **string** |  | [optional] 
**Tags** | **List&lt;string&gt;** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

