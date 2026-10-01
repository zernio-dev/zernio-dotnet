# Zernio.Model.GetAnalyticsDashboard200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DateRange** | [**GetAnalyticsDashboard200ResponseDateRange**](GetAnalyticsDashboard200ResponseDateRange.md) |  | 
**Totals** | [**AnalyticsDashboardTotals**](AnalyticsDashboardTotals.md) |  | 
**PreviousTotals** | [**AnalyticsDashboardTotals**](AnalyticsDashboardTotals.md) |  | [optional] 
**Followers** | [**AnalyticsDashboardFollowers**](AnalyticsDashboardFollowers.md) |  | 
**PreviousFollowers** | [**AnalyticsDashboardFollowers**](AnalyticsDashboardFollowers.md) |  | [optional] 
**Daily** | [**List&lt;GetAnalyticsDashboard200ResponseDailyInner&gt;**](GetAnalyticsDashboard200ResponseDailyInner.md) | One entry per day of the window, days without data included as zeros. | 
**TopPosts** | [**List&lt;AnalyticsDashboardPost&gt;**](AnalyticsDashboardPost.md) |  | 
**RecentPosts** | [**List&lt;AnalyticsDashboardPost&gt;**](AnalyticsDashboardPost.md) |  | 
**DataAsOf** | **DateTime?** | When the most recently synced account in scope was last synced. Null if none has synced yet. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

