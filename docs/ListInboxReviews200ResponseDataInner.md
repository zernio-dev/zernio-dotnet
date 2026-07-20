# Zernio.Model.ListInboxReviews200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Review identifier. For Google Business this is the full review resource name (accounts/{accountId}/locations/{locationId}/reviews/{reviewId}), so it also encodes the location. | [optional] 
**Platform** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**AccountUsername** | **string** |  | [optional] 
**LocationId** | **string** | Bare GBP location id the review belongs to. Google Business only; absent for other platforms. | [optional] 
**LocationName** | **string** | Human-readable GBP location display name. Google Business only; absent for other platforms. | [optional] 
**Reviewer** | [**ListInboxReviews200ResponseDataInnerReviewer**](ListInboxReviews200ResponseDataInnerReviewer.md) |  | [optional] 
**Rating** | **int** |  | [optional] 
**Text** | **string** |  | [optional] 
**Created** | **DateTime** |  | [optional] 
**HasReply** | **bool** |  | [optional] 
**HasPhotos** | **bool** | Whether the review has at least one photo. Google Business only; always false for other platforms. | [optional] 
**PhotoCount** | **int** | Number of photos attached to the review (photos only; videos are not counted). Google Business only; 0 for other platforms. | [optional] 
**Photos** | [**List&lt;GetGoogleBusinessReviews200ResponseReviewsInnerPhotosInner&gt;**](GetGoogleBusinessReviews200ResponseReviewsInnerPhotosInner.md) | Photos attached to the review. Google Business only; always an empty array for other platforms. | [optional] 
**Reply** | [**ListInboxReviews200ResponseDataInnerReply**](ListInboxReviews200ResponseDataInnerReply.md) |  | [optional] 
**ReviewUrl** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

