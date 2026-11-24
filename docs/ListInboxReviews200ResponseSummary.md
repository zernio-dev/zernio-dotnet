# Zernio.Model.ListInboxReviews200ResponseSummary
Computed over every review matching the filters, before pagination. A Facebook Page contributes the Page-wide count and average Facebook reports, which ignore the filters. Google Business Profile locations are computed over the reviews read, partial for accounts in meta.truncatedAccounts.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TotalReviews** | **int** | Includes reviews without a star rating. | [optional] 
**AverageRating** | **decimal?** | Mean star rating rounded to one decimal, leaving out reviews without a star rating. Null when none has one. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

