# Zernio.Model.UpdateAdCampaignStatus200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Status** | **string** | The campaign&#39;s delivery status derived from its switch as read back (&#x60;paused&#x60; when the switch is off). Echoes the request when the platform could not be read. | [optional] 
**PlatformCampaignStatus** | **string** | The campaign&#39;s own switch as read back from the platform, in the raw platform vocabulary (Meta effective_status, TikTok ENABLE / DISABLE, Google ENABLED / PAUSED, ChatGPT (OpenAI) status). Null when the platform could not be read, which is always the case on Pinterest, LinkedIn and X (no single-campaign read). | [optional] 
**StatusReadAt** | **DateTime?** | When the switch was read back. Null when it could not be read. | [optional] 
**Updated** | **int** | 1 when the campaign&#39;s switch was written. | [optional] 
**Skipped** | **int** | 1 when a live read showed the campaign already in the requested state, so nothing was written. | [optional] 
**SkippedReasons** | **List&lt;string&gt;** | Why the write was skipped, for example \&quot;Campaign already switched off\&quot;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

