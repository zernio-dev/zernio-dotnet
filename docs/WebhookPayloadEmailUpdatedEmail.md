# Zernio.Model.WebhookPayloadEmailUpdatedEmail
The message as it is after the change.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MessageId** | **string** |  | [optional] 
**ThreadId** | **string** |  | [optional] 
**Folder** | **string** | &#x60;inbox&#x60;, &#x60;sent&#x60;, &#x60;archive&#x60;, &#x60;trash&#x60;, &#x60;spam&#x60;, &#x60;drafts&#x60;, or the provider folder id for any other folder. | [optional] 
**Unread** | **bool?** |  | [optional] 
**Starred** | **bool?** | Gmail star or Outlook flag. | [optional] 
**Labels** | **List&lt;string&gt;** | Gmail user label ids or Outlook category names. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

