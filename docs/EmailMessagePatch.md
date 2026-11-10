# Zernio.Model.EmailMessagePatch

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | 
**Unread** | **bool** |  | [optional] 
**Starred** | **bool** |  | [optional] 
**Folder** | **string** | Well-known folder name or folder id to move into. | [optional] 
**AddLabels** | **List&lt;string&gt;** | Labels to add, by id or name (case-insensitive). The message stays where it is. On Outlook these are category names; a name not yet in the mailbox is created on the message. | [optional] 
**RemoveLabels** | **List&lt;string&gt;** | Labels to remove, by id or name. A label cannot be both added and removed in one request. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

