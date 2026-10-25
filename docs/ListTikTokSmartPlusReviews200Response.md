# Zernio.Model.ListTikTokSmartPlusReviews200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdAccountId** | **string** |  | [optional] 
**IncludeDeleted** | **bool** |  | [optional] 
**MaxAgeSeconds** | **int** | The freshness window this page was read with. | [optional] 
**Page** | **int** |  | [optional] 
**PageSize** | **int** |  | [optional] 
**TotalPages** | **int** |  | [optional] 
**TotalSmartPlusAds** | **int** | Smart+ ads of the advertiser across all pages. | [optional] 
**Listing** | [**ListTikTokSmartPlusReviews200ResponseListing**](ListTikTokSmartPlusReviews200ResponseListing.md) |  | [optional] 
**ReviewError** | [**ListTikTokSmartPlusReviews200ResponseReviewError**](ListTikTokSmartPlusReviews200ResponseReviewError.md) |  | [optional] 
**Counts** | [**ListTikTokSmartPlusReviews200ResponseCounts**](ListTikTokSmartPlusReviews200ResponseCounts.md) |  | [optional] 
**OldestReadAt** | **DateTime?** | The oldest &#x60;readAt&#x60; in &#x60;items&#x60;. Null when &#x60;items&#x60; is empty. | [optional] 
**Items** | [**List&lt;ListTikTokSmartPlusReviews200ResponseItemsInner&gt;**](ListTikTokSmartPlusReviews200ResponseItemsInner.md) |  | [optional] 
**FailedSmartPlusAds** | [**List&lt;ListTikTokSmartPlusReviews200ResponseFailedSmartPlusAdsInner&gt;**](ListTikTokSmartPlusReviews200ResponseFailedSmartPlusAdsInner.md) | Smart+ ads of this page whose review TikTok refused on its own (for example an ad deleted on TikTok since the listing was read). Zernio splits a refused batch in halves (at most 16 extra calls per page), so the other ads of the batch are still read; ads left unresolved by that cap stay in &#x60;items&#x60; with their stored review or in &#x60;pendingSmartPlusAdIds&#x60;. Empty when none. | [optional] 
**Incomplete** | **bool** | True while some Smart+ ads of this page were never read (&#x60;counts.pending &gt; 0&#x60;). Stale items alone keep it false. | [optional] 
**AllFresh** | **bool** | True when every item and refusal of this page was read within &#x60;maxAgeSeconds&#x60; and nothing is pending. False with &#x60;incomplete: false&#x60; means the page is complete but some reviews are older than the window; a later read refreshes them oldest first. | [optional] 
**PendingSmartPlusAdIds** | **List&lt;string&gt;** | Smart+ ads of this page never read. Empty when every ad has a stored review or refusal. | [optional] 
**RetryAfterSeconds** | **int?** | Seconds to wait before reading this page again, set only while &#x60;incomplete&#x60; is true and review reads are paused. Null when complete (stale items included), or when the page is incomplete without a quota pause (read it again right away). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

