# Zernio.Model.CommentAutomationLog

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**CommentId** | **string** |  | [optional] 
**CommenterId** | **string** |  | [optional] 
**CommenterName** | **string** |  | [optional] 
**CommenterUsername** | **string** |  | [optional] 
**CommentText** | **string** |  | [optional] 
**Source** | **string** | Which door triggered this send. Null on rows written before this field existed (all of those are comment-triggered). | [optional] 
**Status** | **string** | DM outcome. &#39;pending&#39; &#x3D; the automation has a dmDelaySeconds and the response is queued but not sent yet. &#39;gated&#39; &#x3D; the follow-gate confirmation DM went out and we are waiting for the tap; it flips to &#39;sent&#39; or &#39;skipped&#39; when they tap. &#39;skipped&#39; also covers repeatPolicy, cooldown and dedupeSameTextHours suppressions, with the reason in error. | [optional] 
**AudienceOutcome** | **string** | How the audience rule resolved. Null on automations without one. | [optional] 
**GateButtonStatus** | **string** | Whether the follow-gate button reached the commenter: &#39;rejected&#39; &#x3D; Meta refused the gate DM, &#39;omitted&#39; &#x3D; the prompt went out as plain text because it was over 640 characters. Null when no gate DM was sent. | [optional] 
**CommenterIsFollower** | **bool?** | Follow relationship at decision time. Null when Instagram would not tell us (the commenter never messaged the account). | [optional] 
**CommenterFollowerCount** | **int?** |  | [optional] 
**GateResolvedAt** | **DateTime?** | When the follow-gate tap was claimed. | [optional] 
**Error** | **string** | DM error message when status is failed, or the reason when it is skipped. | [optional] 
**PlatformError** | [**CommentAutomationLogPlatformError**](CommentAutomationLogPlatformError.md) |  | [optional] 
**PrivateReplyConsumed** | **bool?** | True when the failed send spent the comment&#39;s single private reply (Instagram subcode 1545133 or 2534023, or Meta code 10900 on Instagram and Facebook), the same rule as &#x60;details.privateReplyConsumed&#x60; on the private-reply endpoint. Null on direct DMs and on rows written before this field existed. | [optional] 
**CommentReplyStatus** | **string** | Outcome of the optional public reply on the triggering comment. With publicReplyPolicy after_dm, &#39;skipped&#39; if no commentReply was configured or if the DM failed (the public reply is not attempted in that case). | [optional] 
**CommentReplyError** | **string** | Public-reply error message if commentReplyStatus is failed | [optional] 
**PublicReplyPostedAt** | **DateTime?** | When the public reply was posted. Null when it was not. | [optional] 
**LikeSkipped** | **string** | Why actions.likeComment did not like the comment. Null when it did or was not configured. | [optional] 
**HideSkipped** | **string** | Why actions.hideComment did not hide the comment. Null when it did or was not configured. | [optional] 
**MediaError** | **string** | Why the dmMedia follow-up was not delivered. The DM itself still counts as sent. | [optional] 
**NextDueAt** | **DateTime?** | When the next queued send fires. Present only while something is still pending. | [optional] 
**ClickedAt** | **DateTime?** | This recipient&#39;s first click on a tracked link (what uniqueClicks counts). | [optional] 
**ClickCount** | **int** | This recipient&#39;s total clicks on tracked links. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

