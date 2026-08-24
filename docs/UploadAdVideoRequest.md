# Zernio.Model.UploadAdVideoRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | 
**AdAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). | 
**VideoUrl** | **string** | Public https URL of the video; downloaded server-side (SSRF-guarded) before chunked upload. Provide exactly one of videoUrl or videoBase64. | [optional] 
**VideoBase64** | **string** | Raw base64 video bytes, or a full data URL (the data:video/...;base64, prefix is stripped). Capped by Vercel&#39;s body limit (~4.5 MB payload). Provide exactly one of videoUrl or videoBase64. | [optional] 
**Filename** | **string** | Optional filename shown alongside the upload session. Applied only when uploading via videoBase64. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

