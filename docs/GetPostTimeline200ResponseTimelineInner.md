# Zernio.Model.GetPostTimeline200ResponseTimelineInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Date** | **DateOnly** | Date in YYYY-MM-DD format | [optional] 
**Platform** | **string** | Platform name (e.g. instagram, tiktok) | [optional] 
**PlatformPostId** | **string** | Platform-specific post ID | [optional] 
**Impressions** | **int** | Total impressions on this date | [optional] 
**Reach** | **int** | Total reach on this date | [optional] 
**Likes** | **int** | Total likes on this date | [optional] 
**Comments** | **int** | Total comments on this date | [optional] 
**Shares** | **int** | Total shares on this date | [optional] 
**Saves** | **int** | Total saves on this date | [optional] 
**Clicks** | **int** | Total clicks on this date | [optional] 
**Views** | **int** | Total views on this date | [optional] 
**Follows** | **int** | Follows attributed to the post on this date (Instagram feed and stories, TikTok business lane); 0 elsewhere | [optional] 
**CompletionRate** | **decimal** | TikTok business lane: share of viewers who watched to the end on this date, 0 to 1; 0 elsewhere | [optional] 
**ProfileViews** | **int** | TikTok business lane: profile views attributed to the post on this date; 0 elsewhere | [optional] 
**WebsiteClicks** | **int** | TikTok business lane: website-link clicks attributed to the post on this date (also inside clicks); 0 elsewhere | [optional] 
**ImpressionSources** | **Dictionary&lt;string, decimal&gt;** | TikTok business lane: share of views by surface on this date (forYou, follow, search, personalProfile, sound, directMessage, other), fractions 0 to 1; empty object elsewhere | [optional] 
**AudienceTypes** | **Dictionary&lt;string, decimal&gt;** | TikTok business lane: follower / nonFollower and newViewer / returnViewer shares on this date, fractions 0 to 1; empty object elsewhere | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

