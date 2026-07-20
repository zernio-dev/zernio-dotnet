# Zernio.Model.BatchGetGoogleBusinessReviewsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**LocationNames** | **List&lt;string&gt;** | Array of full location resource names (e.g. [&#39;accounts/123/locations/456&#39;]). Max 50 per request (Google&#39;s batchGetReviews cap); chunk larger sets into multiple requests. | 
**PageSize** | **int** | Number of reviews per page (max 50) | [optional] [default to 50]
**PageToken** | **string** | Pagination token from previous response | [optional] 
**OrderBy** | **string** | Sort order requested from Google. Defaults to &#39;updateTime desc&#39; (newest first), which allows early-stopping pagination once results cross your date window. | [optional] [default to OrderByEnum.UpdateTimeDesc]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

