# Zernio.Model.WebhookPayloadCommentCommentAuthorInstagramProfile
Instagram only, best-effort. Present ONLY for commenters who have messaged the account before: Meta gates the follow relationship behind messaging consent, and commenting does not grant it. Absent otherwise - treat a missing object as \"unknown\", never as \"not a follower\". To check on demand, call GET /v1/accounts/{accountId}/follow-status/{userId}. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**IsFollower** | **bool?** | The commenter follows this account. | [optional] 
**IsFollowing** | **bool?** | This account follows the commenter. | [optional] 
**FollowerCount** | **int?** |  | [optional] 
**IsVerified** | **bool?** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

