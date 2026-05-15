# Zernio.Model.WebhookPayloadPostPlatformPost

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Content** | **string** |  | 
**Status** | **string** | Post-level status AT FIRE TIME. May still be &#x60;publishing&#x60; if other platforms haven&#39;t terminated; check this field rather than assuming.  | 
**ScheduledFor** | **DateTime** |  | 
**PublishedAt** | **DateTime** |  | [optional] 
**Platforms** | [**List&lt;WebhookPayloadPostPostPlatformsInner&gt;**](WebhookPayloadPostPostPlatformsInner.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

