# Zernio.Model.AccountsListResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Accounts** | [**List&lt;ListedAccount&gt;**](ListedAccount.md) |  | 
**HasAnalyticsAccess** | **bool** | Whether user has analytics add-on access | 
**Pagination** | [**AccountsListResponsePagination**](AccountsListResponsePagination.md) |  | [optional] 
**Warning** | **string** | Only when an unpaged API request was cut at 500 accounts: how to list the rest with cursor paging. | [optional] 
**ProfileTotals** | **Dictionary&lt;string, int&gt;** | Only with profileIds and perProfile. Accounts matching the filters per profile ID; a profile with none is absent. | [optional] 
**StatusCounts** | [**AccountsListResponseStatusCounts**](AccountsListResponseStatusCounts.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

