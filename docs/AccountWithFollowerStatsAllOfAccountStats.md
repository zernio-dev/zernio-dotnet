# Zernio.Model.AccountWithFollowerStatsAllOfAccountStats
Platform-specific account counters from the latest daily snapshot. Each platform reports its own subset of the keys below, and no other key is returned. Absent when the platform reports none of them. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FollowingCount** | **decimal** | Number of accounts being followed (TikTok, X, Pinterest, Bluesky) | [optional] 
**FollowsCount** | **decimal** | Number of accounts being followed (Instagram) | [optional] 
**MediaCount** | **decimal** | Total media posts (Instagram) | [optional] 
**VideoCount** | **decimal** | Total videos (YouTube, TikTok) | [optional] 
**TweetCount** | **decimal** | Total tweets (X) | [optional] 
**PostsCount** | **decimal** | Total posts (Bluesky) | [optional] 
**PinCount** | **decimal** | Total pins (Pinterest) | [optional] 
**TotalViews** | **decimal** | Total channel views (YouTube) | [optional] 
**LikesCount** | **decimal** | Total likes received (TikTok) | [optional] 
**MonthlyViews** | **decimal?** | Monthly profile views (Pinterest). null when Pinterest reports no window | [optional] 
**ListedCount** | **decimal** | Lists the user appears on (X) | [optional] 
**BoardCount** | **decimal** | Total boards (Pinterest) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

