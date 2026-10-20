# Zernio.Model.ListFormLeads200ResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**FormId** | **string** |  | [optional] 
**Source** | **string** | persisted: leads stored from the webhook and the reconcile pass. live: read from Meta because none are stored for this form yet. | [optional] 
**LastCheckedAt** | **DateTime?** | When Zernio last read this form&#39;s leads from Meta. For persisted leads, the last reconcile pass for the Page (null before the first one). For live reads, when the cached Graph read was made. | [optional] 
**LastUpdated** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

