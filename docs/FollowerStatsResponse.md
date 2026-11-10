# Zernio.Model.FollowerStatsResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Accounts** | [**List&lt;AccountWithFollowerStats&gt;**](AccountWithFollowerStats.md) |  | [optional] 
**Stats** | **Dictionary&lt;string, List&lt;FollowerStatsResponseStatsValueInner&gt;&gt;** |  | [optional] 
**DateRange** | [**FollowerStatsResponseDateRange**](FollowerStatsResponseDateRange.md) |  | [optional] 
**Granularity** | **string** |  | [optional] 
**Pagination** | [**AccountCursorPagination**](AccountCursorPagination.md) | Present when limit or cursor is sent, and on the default page of 25 that an API request without accountIds gets. | [optional] 
**Warning** | **string** | Only when the response was cut: the default page of 25 accounts (page through the rest with cursor), or a date range longer than a year (dateRange.from shows where the data starts). Both reasons are joined when they apply together. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

