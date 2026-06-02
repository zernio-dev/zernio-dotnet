# Zernio.Model.ListCommentAutomations200ResponseAutomationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**Trigger** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**PlatformPostId** | **string** |  | [optional] 
**PostTitle** | **string** |  | [optional] 
**Keywords** | **List&lt;string&gt;** |  | [optional] 
**MatchMode** | **string** |  | [optional] 
**DmMessage** | **string** |  | [optional] 
**Buttons** | [**List&lt;DmButton&gt;**](DmButton.md) | Inline DM buttons (up to 3). Omitted when none are set. | [optional] 
**CommentReply** | **string** |  | [optional] 
**LinkTracking** | **bool** | Whether link buttons in the DM are wrapped in a tracked redirect to count clicks. | [optional] 
**ClickTag** | **string** | Tag applied to a contact when they click a tracked link. | [optional] 
**IsActive** | **bool** |  | [optional] 
**Stats** | [**ListCommentAutomations200ResponseAutomationsInnerStats**](ListCommentAutomations200ResponseAutomationsInnerStats.md) |  | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

