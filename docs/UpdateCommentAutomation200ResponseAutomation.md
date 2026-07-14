# Zernio.Model.UpdateCommentAutomation200ResponseAutomation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Keywords** | **List&lt;string&gt;** |  | [optional] 
**MatchMode** | **string** |  | [optional] 
**DmMessage** | **string** |  | [optional] 
**Buttons** | [**List&lt;DmButton&gt;**](DmButton.md) | Inline DM buttons (up to 3). Omitted when none are set. | [optional] 
**CommentReply** | **string** |  | [optional] 
**DmMessageVariations** | **List&lt;string&gt;** | Alternate DM texts rotated at random with dmMessage. Omitted when none. | [optional] 
**CommentReplyVariations** | **List&lt;string&gt;** | Alternate public replies rotated at random with commentReply. Omitted when none. | [optional] 
**IsActive** | **bool** |  | [optional] 
**UpdatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

