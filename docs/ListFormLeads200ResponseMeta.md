# Zernio.Model.ListFormLeads200ResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**FormId** | **string** |  | [optional] 
**Source** | **string** | persisted: leads stored from the webhook and the recovery pass. live: read from Meta because none are stored for this form yet, or because content is not retained. | [optional] 
**LastCheckedAt** | **DateTime?** | For persisted leads, when the recovery pass last finished for the Page (null before the first one). It does not prove every lead is stored. For live reads, when Meta was read. | [optional] 
**LastUpdated** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

