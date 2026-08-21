# Zernio.Model.GetInboxPostComments200ResponseCommentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Message** | **string** |  | [optional] 
**CreatedTime** | **DateTime** |  | [optional] 
**From** | [**GetInboxPostComments200ResponseCommentsInnerFrom**](GetInboxPostComments200ResponseCommentsInnerFrom.md) |  | [optional] 
**LikeCount** | **int** |  | [optional] 
**ReplyCount** | **int** | The platform&#39;s own reply count, which includes hidden and deleted replies. Can exceed replies[].length even when repliesHasMore is false or absent. | [optional] 
**Platform** | **string** | The platform this comment is from | [optional] 
**Url** | **string** | Direct link to the comment on the platform (if available) | [optional] 
**Replies** | **List&lt;Object&gt;** |  | [optional] 
**RepliesHasMore** | **bool** | Facebook only. True when replies[] (capped at 10) does not hold the comment&#39;s full reply thread; fetch the rest by passing the comment id as postId to GET /v1/inbox/comments/{postId}. Absent (not false) on every other platform, including Instagram, which has no equivalent signal. | [optional] 
**CanReply** | **bool** |  | [optional] 
**CanDelete** | **bool** |  | [optional] 
**CanHide** | **bool** | Whether this comment can be hidden (Facebook, Instagram, Threads) | [optional] 
**CanLike** | **bool** | Whether this comment can be liked (Facebook, Twitter/X, Bluesky, Reddit) | [optional] 
**IsHidden** | **bool** | Whether the comment is currently hidden | [optional] 
**IsLiked** | **bool** | Whether the current user has liked this comment | [optional] 
**LikeUri** | **string** | Bluesky like URI for unliking | [optional] 
**Cid** | **string** | Bluesky content identifier | [optional] 
**ParentId** | **string** | ID of the parent comment. Present on entries inside replies[] for Facebook, Instagram and X/Twitter. On X/Twitter it is also present on top-level entries, where it holds the ID of the post replied to. Omitted entirely (key absent, not null) on top-level Facebook and Instagram entries and on every other platform, which express the parent relationship only through replies[] nesting. | [optional] 
**RootUri** | **string** | Bluesky root post URI | [optional] 
**RootCid** | **string** | Bluesky root post CID | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

