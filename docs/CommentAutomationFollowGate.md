# Zernio.Model.CommentAutomationFollowGate
Copy for the follow gate. Sensible defaults are used for any field left empty.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Message** | **string** | Confirmation DM sent when whenUnknown&#x3D;verify. | [optional] 
**ButtonLabel** | **string** | Confirm button label. Defaults to \&quot;I&#39;m following\&quot;. | [optional] 
**NotFollowingMessage** | **string** | Sent to a commenter we know does not follow (followerStatus&#x3D;follower). Omit to stay silent on a keyword comment; a confirm tap always gets an answer. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

