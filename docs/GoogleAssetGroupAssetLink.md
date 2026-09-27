# Zernio.Model.GoogleAssetGroupAssetLink
Link one asset to the asset group. Send exactly one of asset (an existing asset), text, imageUrl or youtubeVideoId (new content, created in the same request).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FieldType** | **string** | Google AssetFieldType, such as HEADLINE, LONG_HEADLINE, DESCRIPTION, BUSINESS_NAME, MARKETING_IMAGE, SQUARE_MARKETING_IMAGE, PORTRAIT_MARKETING_IMAGE, LOGO, LANDSCAPE_LOGO or YOUTUBE_VIDEO. | 
**Asset** | **string** | Existing asset id or resource name customers/{customerId}/assets/{assetId}. Must belong to the campaign&#39;s ad account. | [optional] 
**Text** | **string** | Text assets link as HEADLINE, LONG_HEADLINE, DESCRIPTION or BUSINESS_NAME. | [optional] 
**ImageUrl** | **string** | Public http(s) image. Links as an image role or LOGO / LANDSCAPE_LOGO. | [optional] 
**YoutubeVideoId** | **string** | Links as YOUTUBE_VIDEO. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

