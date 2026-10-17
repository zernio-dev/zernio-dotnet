# Zernio.Model.UploadAdVideoRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id (posting or ads variant); its platform decides where the campaign is created. | 
**AdAccountId** | **string** | Platform ad account id (Meta act_&lt;n&gt;, Google customer id, LinkedIn account id, ...). | 
**VideoUrl** | **string** | Public https URL of the video; downloaded server-side (SSRF-guarded) before chunked upload. Provide exactly one of videoUrl or videoBase64. | [optional] 
**VideoBase64** | **string** | Raw base64 video bytes, or a full data URL (the data:video/...;base64, prefix is stripped). Capped by Vercel&#39;s body limit (~4.5 MB payload). Provide exactly one of videoUrl or videoBase64. | [optional] 
**Filename** | **string** | Optional file name, sent to Meta as the video&#39;s name and title so it shows and is searchable in the Ads Manager media library. Applies to both videoUrl and videoBase64. Without it (and without name), a videoUrl upload is named after the last path segment of the URL. | [optional] 
**Name** | **string** | Optional video name shown in the Ads Manager media library. Takes precedence over filename. | [optional] 
**Async** | **bool** | true: answer 202 once Meta accepts the upload instead of waiting for processing. Poll GET /v1/ads/videos/{videoId} or subscribe to ad.video.processed. | [optional] [default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

