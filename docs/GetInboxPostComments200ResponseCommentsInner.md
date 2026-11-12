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
**RepliesHasMore** | **bool** | Facebook only. True when replies[] (capped at 10) does not hold the comment&#39;s full reply thread.  Fetch the rest by passing the comment id as the &#x60;commentId&#x60; query parameter to GET /v1/inbox/comments/{postId} (or, for backwards compatibility, as &#x60;postId&#x60;).  Absent (not false) on every other platform, including Instagram, which has no equivalent signal, except with view&#x3D;summary, where it is also true on any comment whose &#x60;replyCount&#x60; is higher than the replies it carries (nested replies are cut to 3 there).  | [optional] 
**CanReply** | **bool** | Whether this comment can be replied to. Always present. | [optional] 
**CanDelete** | **bool** | Whether DELETE is expected to work on this comment. True for the account&#39;s own comments, and for anyone&#39;s comment on Facebook, Instagram, YouTube and LinkedIn organization accounts. On TikTok, TikTok&#39;s own flag decides. False does not block the call: the platform decides. Always present. | [optional] 
**CanHide** | **bool** | Whether hide is supported for this comment&#39;s platform (Facebook, Instagram, Threads, X, TikTok). It does not check each comment: X needs a conversation started by the account, and Threads only hides top-level replies. Always present. | [optional] 
**CanLike** | **bool** | Whether this comment can be liked (Facebook, X, Bluesky, Reddit, LinkedIn, TikTok). Always present. | [optional] 
**IsHidden** | **bool** | Whether the comment is currently hidden. On Instagram accounts connected through Facebook Login, Meta leaves hidden comments (and their replies) out of the list entirely, so they never appear with isHidden true; Instagram Login accounts and Facebook Pages return them with isHidden true. | [optional] 
**IsLiked** | **bool** | Whether the current user has liked this comment | [optional] 
**Attachment** | [**CommentAttachment**](CommentAttachment.md) | The comment&#39;s media, whenever the platform returns one (replies included). Supported on Facebook, TikTok, X, Threads and Bluesky; absent when the comment has no media and on every other platform. See CommentAttachment for each platform&#39;s &#x60;type&#x60; values. | [optional] 
**LikeUri** | **string** | Bluesky like URI for unliking | [optional] 
**Cid** | **string** | Bluesky content identifier | [optional] 
**ParentId** | **string** | ID of the parent comment.  - Facebook and Instagram: present on entries inside replies[]; omitted on top-level entries. - X: present inside replies[] and on top-level entries, where it holds the ID of the post replied to. - Every other platform: omitted; the parent relationship is expressed only through replies[] nesting.  When omitted, the key is absent, not null. | [optional] 
**RootUri** | **string** | Bluesky root post URI | [optional] 
**RootCid** | **string** | Bluesky root post CID | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

