# Zernio.Model.GetInboxPostComments200ResponsePost
(Reddit only) Metadata for the target post, returned alongside the comments in Reddit's single round-trip. Lets integrators render a preview of the post the user is commenting on without an additional request. Absent for non-Reddit platforms and when the upstream response is missing the post listing (deleted post, malformed response). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Reddit post base36 id (e.g. \&quot;1tjtj26\&quot;) | [optional] 
**Fullname** | **string** | Fullname with type prefix (e.g. \&quot;t3_1tjtj26\&quot;) | [optional] 
**Title** | **string** |  | [optional] 
**Selftext** | **string** | Body text for self-posts (empty for link posts) | [optional] 
**Author** | **string** | Reddit username | [optional] 
**Subreddit** | **string** | Subreddit name | [optional] 
**Permalink** | **string** | Absolute URL to the post on reddit.com | [optional] 
**Url** | **string** | For link posts | [optional] 
**Score** | **int** | Net upvotes (upvotes minus downvotes) | [optional] 
**NumComments** | **int** |  | [optional] 
**CreatedUtc** | **int** | Unix timestamp in seconds | [optional] 
**Over18** | **bool** |  | [optional] 
**Stickied** | **bool** |  | [optional] 
**FlairText** | **string** | Link flair text if any | [optional] 
**IsGallery** | **bool** | True if the post is a Reddit gallery (multiple images) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

