# Zernio.Model.GetYoutubeCaptions200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | [optional] 
**VideoId** | **string** |  | [optional] 
**Language** | **string** | The language of the returned track. | [optional] 
**TrackId** | **string** | YouTube&#39;s own caption track id. | [optional] 
**TrackKind** | **string** | &#x60;asr&#x60; is YouTube&#39;s auto-generated track; &#x60;standard&#x60; was uploaded by the channel. | [optional] 
**Source** | **string** | &#x60;cache&#x60; when served from our stored copy, &#x60;youtube&#x60; when this call spent the quota units. | [optional] 
**FetchedAt** | **DateTime** | When the stored copy was downloaded from YouTube. | [optional] 
**Text** | **string** | The whole transcript as one paragraph, no timings. | [optional] 
**Cues** | [**List&lt;GetYoutubeCaptions200ResponseCuesInner&gt;**](GetYoutubeCaptions200ResponseCuesInner.md) | Timed cues. Present when format is json. Auto-generated cues overlap in time by design (captions roll), so &#x60;start&#x60; can precede the previous cue&#39;s &#x60;end&#x60;. | [optional] 
**Srt** | **string** | Raw SubRip body. Present when format is srt. | [optional] 
**AvailableTracks** | [**List&lt;GetYoutubeCaptions200ResponseAvailableTracksInner&gt;**](GetYoutubeCaptions200ResponseAvailableTracksInner.md) | Every track on the video, so you can re-request another language. On a cached read this is the listing as it stood when we downloaded, so a language added to the video since then appears only after a &#x60;refresh&#x3D;true&#x60; or when you request that language directly. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

