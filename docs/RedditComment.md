# Zernio.Model.RedditComment
One comment of a Reddit thread as returned by GET /v1/reddit/comments/{postId}; the list is flat and in thread order

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Reddit comment ID (without type prefix) | [optional] 
**Fullname** | **string** | Reddit fullname (e.g. t1_abc123) | [optional] 
**ParentId** | **string** | Fullname of what the comment answers: the post (t3_…) or a parent comment (t1_…) | [optional] 
**Author** | **string** | The username, or [deleted] | [optional] 
**Body** | **string** | Comment text as written (Markdown, not HTML-escaped), or [deleted] / [removed] | [optional] 
**Permalink** | **string** | Full permalink to the comment | [optional] 
**CreatedUtc** | **decimal** | Unix timestamp of the comment | [optional] 
**Score** | **int** |  | [optional] 
**NumReplies** | **int** | Direct replies included in this response; replies Reddit left out are listed in more | [optional] 
**Depth** | **int** | 0 for a top-level comment of this response, 1 for a reply to it, and so on | [optional] 
**IsSubmitter** | **bool** | Whether the author is the post&#39;s author | [optional] 
**Edited** | **bool** |  | [optional] 
**Stickied** | **bool** |  | [optional] 
**Distinguished** | **string** | \&quot;moderator\&quot; or \&quot;admin\&quot; when the comment is distinguished, else null | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

