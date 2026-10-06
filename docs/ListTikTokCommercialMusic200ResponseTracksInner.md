# Zernio.Model.ListTikTokCommercialMusic200ResponseTracksInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The full track&#39;s song clip id. Accepted as musicSoundId, but prefer clip.id: posts published with this id have shown viewers a sound page saying the song is not available in their country (observed from Germany). TikTok rejects the commercial music id itself at publish time. | [optional] 
**CommercialMusicId** | **string** | TikTok&#39;s commercial_music_id, for reference only | [optional] 
**Name** | **string** |  | [optional] 
**Artist** | **string** |  | [optional] 
**DurationSec** | **int** |  | [optional] 
**Genres** | **List&lt;string&gt;** |  | [optional] 
**PreviewUrl** | **string** | Preview audio of the full track | [optional] 
**ThumbnailUrl** | **string** |  | [optional] 
**Rank** | **int** | Position in the trending chart, 1 first | [optional] 
**Clip** | [**ListTikTokCommercialMusic200ResponseTracksInnerClip**](ListTikTokCommercialMusic200ResponseTracksInnerClip.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

