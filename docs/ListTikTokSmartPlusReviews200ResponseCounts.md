# Zernio.Model.ListTikTokSmartPlusReviews200ResponseCounts
The Smart+ ads on this page split by state; the four counts add up to the Smart+ ads on this page (fewer than `pageSize` on the last page).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Fresh** | **int** | Items read within &#x60;maxAgeSeconds&#x60;. | [optional] 
**Stale** | **int** | Items read earlier, returned with their &#x60;readAt&#x60; and due for a refresh. | [optional] 
**Pending** | **int** | Smart+ ads never read (&#x60;pendingSmartPlusAdIds&#x60;). | [optional] 
**Failed** | **int** | Entries of &#x60;failedSmartPlusAds&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

