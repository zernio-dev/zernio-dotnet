# Zernio.Model.BulkCreateContactsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** |  | 
**AccountId** | **string** | Required when contacts carry channel data (platformIdentifier or a row-level accountId). Omit for a plain CRM import with no channels. | [optional] 
**Platform** | **string** | Ignored when accountId is set: the platform is derived from the resolved account. Only relevant to disambiguate accountId lookup; a mismatch 404s. | [optional] 
**Contacts** | [**List&lt;BulkCreateContactsRequestContactsInner&gt;**](BulkCreateContactsRequestContactsInner.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

