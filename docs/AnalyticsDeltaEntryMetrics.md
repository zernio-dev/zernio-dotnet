# Zernio.Model.AnalyticsDeltaEntryMetrics
Metrics a platform does not report are 0, not absent.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Impressions** | **int** |  | 
**Reach** | **int** |  | 
**Likes** | **int** |  | 
**Comments** | **int** |  | 
**Shares** | **int** |  | 
**Saves** | **int** |  | 
**Sends** | **int** |  | 
**Clicks** | **int** |  | 
**Views** | **int** |  | 
**Follows** | **int** | Follows attributed to this post (Instagram) | 
**IgReelsAvgWatchTime** | **int** | Instagram Reels average watch time, in milliseconds | 
**IgReelsVideoViewTotalTime** | **int** | Instagram Reels total watch time, in milliseconds | 
**Reposts** | **int** |  | 
**ReelsSkipRate** | **decimal** | Instagram Reels skip rate, 0 to 1 | 
**CompletionRate** | **decimal** | TikTok business lane: share of viewers who watched to the end, 0 to 1 | 
**ProfileViews** | **int** | TikTok business lane: profile views attributed to the post | 
**WebsiteClicks** | **int** | TikTok business lane: website-link clicks attributed to the post (also inside clicks) | 
**ImpressionSources** | **Dictionary&lt;string, decimal&gt;** | TikTok business lane: share of views by surface (forYou, follow, search, personalProfile, sound, directMessage, other), fractions 0 to 1. Empty object elsewhere. | 
**AudienceTypes** | **Dictionary&lt;string, decimal&gt;** | TikTok business lane: follower / nonFollower and newViewer / returnViewer shares, fractions 0 to 1. Empty object elsewhere. | 
**AudienceCountries** | **Dictionary&lt;string, decimal&gt;** | TikTok business lane: viewer-country shares keyed by ISO-3166 alpha-2, fractions 0 to 1, top 20 with the tail in &#x60;other&#x60;. Empty object elsewhere. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

