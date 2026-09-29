# Zernio.Model.UpdateAdSetStatus200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Status** | **string** | The ad set&#39;s delivery status derived from the switches read back: &#x60;paused&#x60; when its own switch or its campaign&#39;s switch is off. Echoes the request when the platform could not be read. | [optional] 
**PlatformAdSetStatus** | **string** | The ad set&#39;s own switch as read back from the platform, in the raw platform vocabulary (Meta effective_status, TikTok ENABLE / DISABLE, Google ENABLED / PAUSED, LinkedIn and Pinterest ACTIVE / PAUSED, ChatGPT (OpenAI) status). Null when the platform could not be read, which is always the case on X. | [optional] 
**PlatformCampaignStatus** | **string** | The parent campaign&#39;s switch, read in the same call where the platform returns it, otherwise the stored value. | [optional] 
**StatusReadAt** | **DateTime?** | When the ad set switch was read back. Null when it could not be read. | [optional] 
**Updated** | **int** | 1 when the ad set&#39;s switch was written. | [optional] 
**Skipped** | **int** | 1 when a live read showed the ad set already in the requested state, so nothing was written. | [optional] 
**SkippedReasons** | **List&lt;string&gt;** | Why the write was skipped, for example \&quot;Ad set already switched off\&quot;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

