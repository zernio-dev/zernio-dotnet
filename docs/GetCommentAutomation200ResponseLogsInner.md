# Zernio.Model.GetCommentAutomation200ResponseLogsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**CommentId** | **string** |  | [optional] 
**CommenterId** | **string** |  | [optional] 
**CommenterName** | **string** |  | [optional] 
**CommentText** | **string** |  | [optional] 
**Source** | **string** | Which door triggered this send. Absent on rows written before this field existed (all of those are comment-triggered). | [optional] 
**Status** | **string** | DM outcome. &#39;pending&#39; &#x3D; the automation has a dmDelaySeconds and the response is queued but not sent yet. &#39;gated&#39; &#x3D; the follow-gate confirmation DM went out and we are waiting for the tap; it flips to &#39;sent&#39; or &#39;skipped&#39; when they tap. | [optional] 
**AudienceOutcome** | **string** | How the audience rule resolved. Absent on automations without one. | [optional] 
**CommenterIsFollower** | **bool** | Follow relationship at decision time. Absent when Instagram would not tell us (the commenter never messaged the account). | [optional] 
**CommenterFollowerCount** | **int** |  | [optional] 
**Error** | **string** | DM error message if status is failed | [optional] 
**CommentReplyStatus** | **string** | Outcome of the optional public reply on the triggering comment. &#39;skipped&#39; if no commentReply was configured or if the DM failed (the public reply is not attempted in that case). | [optional] 
**CommentReplyError** | **string** | Public-reply error message if commentReplyStatus is failed | [optional] 
**NextDueAt** | **DateTime** | When the next queued send fires. Present only while something is still pending. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

