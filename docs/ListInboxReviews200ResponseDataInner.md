# Zernio.Model.ListInboxReviews200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**AccountUsername** | **string** |  | [optional] 
**Reviewer** | [**ListInboxReviews200ResponseDataInnerReviewer**](ListInboxReviews200ResponseDataInnerReviewer.md) |  | [optional] 
**Rating** | **int** |  | [optional] 
**Text** | **string** |  | [optional] 
**Created** | **DateTime** |  | [optional] 
**HasReply** | **bool** |  | [optional] 
**HasPhotos** | **bool** | Whether the review has at least one photo. Google Business only; always false for other platforms. | [optional] 
**PhotoCount** | **int** | Number of photos attached to the review (photos only; videos are not counted). Google Business only; 0 for other platforms. | [optional] 
**Reply** | [**ListInboxReviews200ResponseDataInnerReply**](ListInboxReviews200ResponseDataInnerReply.md) |  | [optional] 
**ReviewUrl** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

