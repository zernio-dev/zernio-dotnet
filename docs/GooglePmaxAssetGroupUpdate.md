# Zernio.Model.GooglePmaxAssetGroupUpdate
Replacement assets for an existing Performance Max asset group, sent on PUT /v1/ads/{adId}. Google assets are immutable (AssetService only creates), so each field you send becomes new assets linked to the asset group, and the assets that role held are unlinked in the same atomic request. Send one field or many; a field you omit is left untouched. Re-sending a value the asset group already carries is a no-op for that asset, not a re-upload. Unlinked assets stay in the account's asset library: Google has no asset delete. At least one description must be 60 characters or fewer. Texts within each list must be distinct. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FinalUrl** | **string** | Replaces the asset group&#39;s final URL. | [optional] 
**Headlines** | **List&lt;string&gt;** | Replaces every HEADLINE asset on the group. | [optional] 
**LongHeadline** | **string** | Replaces the LONG_HEADLINE asset. | [optional] 
**Descriptions** | **List&lt;string&gt;** | Replaces every DESCRIPTION asset. At least one must be 60 characters or fewer. | [optional] 
**BusinessName** | **string** | Replaces the BUSINESS_NAME asset. | [optional] 
**Images** | [**GooglePmaxAssetGroupUpdateImages**](GooglePmaxAssetGroupUpdateImages.md) |  | [optional] 
**YoutubeVideoIds** | **List&lt;string&gt;** | Replaces YOUTUBE_VIDEO assets with existing YouTube video ids. Video uploads and arbitrary video URLs are not supported. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

