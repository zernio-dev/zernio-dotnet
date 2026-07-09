# Zernio.Model.SetCommentModerationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | The social account ID | 
**Platform** | **string** | Only YouTube supports comment moderation | 
**ModerationStatus** | **string** | published approves the comment, rejected removes it, heldForReview returns it to the queue. | 
**BanAuthor** | **bool** | Also ban the comment&#39;s author, auto-rejecting their future comments. Only valid when moderationStatus is \&quot;rejected\&quot;; any other pairing is a 400.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

