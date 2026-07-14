# Zernio.Model.UpdateCommentAutomationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | [optional] 
**Keywords** | **List&lt;string&gt;** |  | [optional] 
**MatchMode** | **string** |  | [optional] 
**DmMessage** | **string** |  | [optional] 
**Buttons** | [**List&lt;DmButton&gt;**](DmButton.md) | Inline DM buttons (1-3). Pass [] to clear all buttons. | [optional] 
**CommentReply** | **string** |  | [optional] 
**DmMessageVariations** | **List&lt;string&gt;** | Alternate DM texts for random rotation (see create). Pass [] to clear. | [optional] 
**CommentReplyVariations** | **List&lt;string&gt;** | Alternate public replies for random rotation. Pass [] to clear. | [optional] 
**LinkTracking** | **bool** | Wrap link buttons in a tracked redirect to count clicks. Pass false to send links untouched. | [optional] 
**ClickTag** | **string** | Tag applied to a contact when they click a tracked link (requires linkTracking). Empty string clears it. | [optional] 
**IsActive** | **bool** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

