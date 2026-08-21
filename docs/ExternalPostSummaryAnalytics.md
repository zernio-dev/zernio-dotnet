# Zernio.Model.ExternalPostSummaryAnalytics
Engagement + insights for the post. `likes` and `comments` are available immediately after an on-demand sync (they come from the platform listing). `reach`, `impressions`, `views` depend on the platform's insights, which carry their own delay (e.g. ~24h on Instagram) and read 0 until the platform makes them available. 

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

