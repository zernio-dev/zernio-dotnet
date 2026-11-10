# Zernio.Model.EmailSharedMailbox
An Outlook shared mailbox added under a connected Microsoft account. It is an account of its own, so every `/v1/email` endpoint takes its `accountId`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Pass it as &#x60;accountId&#x60; to any /v1/email endpoint. | [optional] 
**Address** | **string** |  | [optional] 
**DisplayName** | **string** |  | [optional] 
**ParentAccountId** | **string** | The Outlook account whose access opens this mailbox. | [optional] 
**IsActive** | **bool** |  | [optional] 
**AddedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

