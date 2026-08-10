# Zernio.Model.InstagramAudioAsset
One asset from the Instagram audio catalog. Licensed music carries artist/artwork fields; original sounds carry creator fields instead, so most fields are nullable.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AudioId** | **string** | Audio asset ID. Pass it as platformSpecificData.audioConfiguration.audioId when creating a Reel. | [optional] 
**Title** | **string** | Track or sound title. | [optional] 
**AudioType** | **string** | Catalog type of the asset. | [optional] 
**DurationInMs** | **int?** | Asset duration in milliseconds. | [optional] 
**DisplayArtist** | **string** | Artist name (licensed music only). | [optional] 
**CoverArtworkThumbnailUrl** | **string** | Cover artwork thumbnail (licensed music only). | [optional] 
**DownloadUrl** | **string** | Temporary preview URL. Meta expires it after roughly 1.5 days; re-fetch the asset to refresh it. | [optional] 
**IgUsername** | **string** | Creator username (original sounds only). | [optional] 
**ProfilePictureUrl** | **string** | Creator profile picture (original sounds only). | [optional] 
**IsAdsEligible** | **bool?** | Whether the asset is eligible for ads use. | [optional] 
**OnPlatformAudioPreviewLink** | **string** | Instagram web link to preview the audio. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

