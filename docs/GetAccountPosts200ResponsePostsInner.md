# Zernio.Model.GetAccountPosts200ResponsePostsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The platform&#39;s own post id (the video ID on YouTube) | [optional] 
**Platform** | **string** |  | [optional] 
**Message** | **string** | Caption or title, empty string when the post has no text | [optional] 
**CreatedTime** | **DateTime** |  | [optional] 
**Permalink** | **string** | Public URL of the post on the platform | [optional] 
**Picture** | **string** | Thumbnail or media URL | [optional] 
**MediaType** | **string** |  | [optional] 
**CommentCount** | **int** |  | [optional] 
**LikeCount** | **int** |  | [optional] 
**ReactionCount** | **int** | Facebook and LinkedIn only | [optional] 
**ShareCount** | **int** |  | [optional] 
**Cid** | **string** | Bluesky content id, required to reply to the post | [optional] 
**Subreddit** | **string** | Reddit only | [optional] 
**Title** | **string** | Pinterest only: native Pin title | [optional] 
**Description** | **string** | Pinterest only: full native Pin description (Pinterest caps it at 800 characters) | [optional] 
**Link** | **string** | Pinterest only: destination URL of the Pin, not the Pin page (see permalink) | [optional] 
**BoardId** | **string** | Pinterest only: id of the board holding the Pin | [optional] 
**BoardOwnerUsername** | **string** | Pinterest only: username of the board owner | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

