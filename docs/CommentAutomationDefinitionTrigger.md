# Zernio.Model.CommentAutomationDefinitionTrigger

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** | &#x60;comment.keyword&#x60; for a comment on a post or reel. The &#x60;comment.received&#x60; event starts an event automation, not comment to DM. | 
**ProfileId** | **string** |  | 
**AccountId** | **string** | The account it answers on, on the profile. It cannot change once saved. | 
**PlatformPostId** | **string** | The platform post or story it answers. Null answers every one. One active automation per post. | [optional] 
**PostId** | **string** | A Zernio post. A scheduled one is answered once it publishes. | [optional] 
**PostTitle** | **string** |  | [optional] 
**Filter** | [**CommentAutomationFilter**](CommentAutomationFilter.md) |  | 
**Entry** | **List&lt;string&gt;** | The nodes a run starts at. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

