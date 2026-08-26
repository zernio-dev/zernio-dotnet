# Zernio.Model.GoogleBusinessReview
A Google Business Profile review, as returned by every gmb-reviews read endpoint.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Review ID | [optional] 
**Name** | **string** | Full resource name | [optional] 
**Reviewer** | [**GoogleBusinessReviewReviewer**](GoogleBusinessReviewReviewer.md) |  | [optional] 
**Rating** | **int** | Numeric star rating (0 when Google sends no rating) | [optional] 
**StarRating** | **string** | Google&#39;s string rating | [optional] 
**Comment** | **string** | Review text | [optional] 
**CreateTime** | **DateTime** |  | [optional] 
**UpdateTime** | **DateTime** |  | [optional] 
**ReviewReply** | [**GoogleBusinessReviewReviewReply**](GoogleBusinessReviewReviewReply.md) |  | [optional] 
**PhotoCount** | **int** | Number of photos attached to the review (photos only, videos are not counted) | [optional] 
**Photos** | [**List&lt;ListInboxReviews200ResponseDataInnerPhotosInner&gt;**](ListInboxReviews200ResponseDataInnerPhotosInner.md) | Photos attached to the review by the reviewer | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

