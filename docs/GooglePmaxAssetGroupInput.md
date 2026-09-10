# Zernio.Model.GooglePmaxAssetGroupInput
Google Performance Max creative assets. At least one description must be 60 characters or fewer. Texts within each list must be distinct.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Defaults to the request name. | [optional] 
**FinalUrl** | **string** | Required destination URL. | 
**Headlines** | **List&lt;string&gt;** |  | 
**LongHeadline** | **string** |  | 
**Descriptions** | **List&lt;string&gt;** | At least one description must be 60 characters or fewer. | 
**BusinessName** | **string** |  | 
**Images** | [**GooglePmaxAssetGroupInputImages**](GooglePmaxAssetGroupInputImages.md) |  | 
**YoutubeVideoId** | **string** | Optional existing YouTube video id. Google can generate video when omitted. Video uploads and arbitrary video URLs are not supported. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

