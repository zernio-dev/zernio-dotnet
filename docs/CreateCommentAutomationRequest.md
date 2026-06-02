# Zernio.Model.CreateCommentAutomationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** |  | 
**AccountId** | **string** | Instagram or Facebook account ID | 
**Trigger** | **string** | What fires the automation. &#39;comment&#39; (keyword comment on a post) or &#39;story_reply&#39; (keyword reply to an Instagram story). For &#39;story_reply&#39;, platformPostId is the story media id (omit for any story). | [optional] [default to TriggerEnum.Comment]
**PlatformPostId** | **string** | Platform media/post ID (or story media id when trigger&#x3D;story_reply). Omit for an account-wide (any-post / any-story) automation. | [optional] 
**PostId** | **string** | Zernio post ID. Required only when also targeting a specific post via platformPostId. | [optional] 
**PostTitle** | **string** | Post content snippet for display | [optional] 
**Name** | **string** | Automation label | 
**Keywords** | **List&lt;string&gt;** | Trigger keywords (empty &#x3D; any comment triggers) | [optional] 
**MatchMode** | **string** |  | [optional] [default to MatchModeEnum.Contains]
**DmMessage** | **string** | DM text to send to commenter. Max 640 chars when buttons are set, otherwise ~1000. | 
**Buttons** | [**List&lt;DmButton&gt;**](DmButton.md) | Optional inline DM buttons (1-3). Phone buttons are Facebook-only. Omit or pass [] for a plain-text DM. | [optional] 
**CommentReply** | **string** | Optional public reply to the comment | [optional] 
**LinkTracking** | **bool** | Wrap link buttons in the DM in a tracked redirect so clicks are counted (Link Clicks / CTR). Pass false to send links exactly as written. Defaults to on. | [optional] [default to true]
**ClickTag** | **string** | Optional tag applied to a contact when they click a tracked link (requires linkTracking). Lets you segment clickers for broadcasts/sequences. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

