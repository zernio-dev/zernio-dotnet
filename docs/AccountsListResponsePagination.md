# Zernio.Model.AccountsListResponsePagination
Present on a paginated request: `{ page, limit, total, pages }` with page and limit, `{ limit, nextCursor }` with cursor paging (limit alone or cursor).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Page** | **int** |  | [optional] 
**Limit** | **int** |  | 
**Total** | **int** |  | [optional] 
**Pages** | **int** |  | [optional] 
**NextCursor** | **string** | Opaque cursor for the next page; pass it back as &#x60;cursor&#x60;. Null on the last page. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

