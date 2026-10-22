# Zernio.Model.TikTokSmartPlusMaterialReview
The verdict of one creative of a Smart+ ad (`material_review_infos`).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdMaterialId** | **string** | TikTok &#x60;ad_material_id&#x60; of the creative inside this ad. | [optional] 
**MaterialType** | **string** | Null for a creative TikTok added on its own or a carousel image. | [optional] 
**TiktokItemId** | **string** | The TikTok post id when the creative is a Spark post. | [optional] 
**VideoId** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**OperationStatus** | **string** | TikTok &#x60;material_operation_status&#x60;: ENABLE or DISABLE. | [optional] 
**ReviewStatus** | **TikTokSmartPlusReviewStatus** |  | [optional] 
**RawReviewStatus** | **string** | TikTok &#x60;review_status&#x60;, verbatim. | [optional] 
**RejectReasons** | **List&lt;string&gt;** | Every distinct reason across &#x60;rejections&#x60;. Empty when approved. | [optional] 
**PassedLocations** | **List&lt;string&gt;** |  | [optional] 
**Rejections** | [**List&lt;TikTokReviewRejection&gt;**](TikTokReviewRejection.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

