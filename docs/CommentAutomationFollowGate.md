# Zernio.Model.CommentAutomationFollowGate
Copy for the follow gate. Sensible defaults are used for any field left empty.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Message** | **string** | Confirmation DM sent when whenUnknown&#x3D;verify. | [optional] 
**ButtonLabel** | **string** | Confirm button label. Defaults to \&quot;I&#39;m following\&quot;. | [optional] 
**NotFollowingMessage** | **string** | Sent to a commenter we know does not follow (followerStatus&#x3D;follower), and after a confirm tap that does not unlock the DM. When following is what would unlock it, the message carries the confirm button so they can re-check once they follow; above 640 characters it goes out as plain text without the button. Omit to stay silent on a keyword comment; a confirm tap always gets an answer (a default message is used). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

