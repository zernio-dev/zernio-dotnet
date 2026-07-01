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
**EngagementRate** | **decimal** |  | [optional] 
**LastUpdated** | **DateTime** | When these metrics were last refreshed | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

