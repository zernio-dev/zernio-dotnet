# Zernio.Model.UpdateCommentAutomationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | [optional] 
**Trigger** | **string** | What fires the automation. Changing it detaches the automation from its bound post or story (a post id and a story id are different objects), unless this same request sets a new binding. &#39;story_reply&#39; is Instagram only. | [optional] 
**Keywords** | **List&lt;string&gt;** |  | [optional] 
**MatchMode** | **string** | How a keyword is compared with the comment. &#39;contains&#39; (default) matches anywhere, even inside another word (keyword &#39;app&#39; fires on &#39;happy&#39;). &#39;word&#39; matches the keyword only as a standalone word. &#39;exact&#39; requires the whole comment to be exactly the keyword. | [optional] 
**ExcludeKeywords** | **List&lt;string&gt;** | Comments containing one of these never trigger the automation, even when a trigger keyword also matches. Compared using the same matchMode. | [optional] 
**TypoTolerance** | **bool** | Only with matchMode&#x3D;word: also fire on close misspellings of a keyword (one edit for 4-7 character keywords, two from 8 up). Keywords shorter than 4 characters are never fuzzy-matched. | [optional] 
**DmMessage** | **string** |  | [optional] 
**Buttons** | [**List&lt;DmButton&gt;**](DmButton.md) | Inline DM buttons (1-3). Pass [] to clear all buttons. | [optional] 
**CommentReply** | **string** |  | [optional] 
**DmMessageVariations** | **List&lt;string&gt;** | Alternate DM texts for random rotation (see create). Pass [] to clear. | [optional] 
**CommentReplyVariations** | **List&lt;string&gt;** | Alternate public replies for random rotation. Pass [] to clear. | [optional] 
**LinkTracking** | **bool** | Wrap link buttons in a tracked redirect to count clicks. Pass false to send links untouched. | [optional] 
**ClickTag** | **string** | Tag applied to a contact when they click a tracked link (requires linkTracking). Empty string clears it. | [optional] 
**DmDelaySeconds** | **int** | Seconds to wait after the trigger before sending the DM. Send 0 to clear the delay and reply immediately. | [optional] 
**CommentReplyDelaySeconds** | **int** | Seconds to wait before posting the public comment reply. Send 0 to clear it. The reply never goes out before the DM. | [optional] 
**Audience** | [**CommentAutomationAudience**](CommentAutomationAudience.md) |  | [optional] 
**FollowGate** | [**CommentAutomationFollowGate**](CommentAutomationFollowGate.md) |  | [optional] 
**IsActive** | **bool** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

