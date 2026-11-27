# Zernio.Model.ExternalPostSummaryAnalytics
Not a source of metrics: read a post's metrics from GET /v1/analytics.  - A post read from Zernio's records (the recent posts list, or a   matched post that was already stored): usually `null` or only   `lastUpdated`. - Archived Instagram stories and posts first synced before metrics   moved to GET /v1/analytics: metric fields that are final or no   longer refreshed. Do not use them. - A post imported by this call (a LinkedIn personal profile post, a   TikTok Business post or a Pinterest Pin fetched by `url`/`postId`):   the values just fetched. A LinkedIn re-import of the same post   within about 15 seconds returns the stored record without metrics. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Likes** | **int** |  | [optional] 
**Comments** | **int** |  | [optional] 
**Shares** | **int** |  | [optional] 
**Saves** | **int** |  | [optional] 
**Sends** | **int** |  | [optional] 
**Clicks** | **int** |  | [optional] 
**Views** | **int** |  | [optional] 
**Reach** | **int** |  | [optional] 
**Impressions** | **int** |  | [optional] 
**EngagementRate** | **decimal** | Percentage, rounded to 2 decimals. Same definition as PostAnalytics.engagementRate: (likes + comments + shares + saves) / (impressions or reach or views) * 100, where the denominator is the first of the three that is non-zero. Clicks and follows are never counted. | [optional] 
**LastUpdated** | **DateTime** | When these metrics were last refreshed | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

