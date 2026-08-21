# Zernio.Model.LinkedInAggregateAnalyticsTotalResponseAnalytics

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Impressions** | **int** | Total impressions across all posts | [optional] 
**Reach** | **int** | Unique members reached across all posts | [optional] 
**Reactions** | **int** | Total reactions across all posts | [optional] 
**Comments** | **int** | Total comments across all posts | [optional] 
**Shares** | **int** | Total reshares across all posts | [optional] 
**Saves** | **int** | Total times posts were saved (personal accounts only) | [optional] 
**Sends** | **int** | Total times posts were sent via LinkedIn messaging (personal accounts only) | [optional] 
**EngagementRate** | **decimal** | Overall engagement rate, as a percentage rounded to 2 decimals: (reactions + comments + shares + saves + sends) / impressions * 100. Clicks are not counted, and there is no fallback denominator, so this is 0 whenever impressions is 0. This is NOT the same formula as PostAnalytics.engagementRate on GET /v1/analytics. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

