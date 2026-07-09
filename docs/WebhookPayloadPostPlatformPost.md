# Zernio.Model.WebhookPayloadPostPlatformPost

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Content** | **string** |  | 
**Status** | **string** | Post-level status AT FIRE TIME. May still be &#x60;publishing&#x60; if other platforms haven&#39;t terminated; check this field rather than assuming.  | 
**ScheduledFor** | **DateTime** |  | 
**PublishedAt** | **DateTime** |  | [optional] 
**Platforms** | [**List&lt;WebhookPayloadPostPlatformPostPlatformsInner&gt;**](WebhookPayloadPostPlatformPostPlatformsInner.md) |  | 
**Metadata** | **Dictionary&lt;string, Object&gt;** | The free-form &#x60;metadata&#x60; object supplied when the post was created, echoed back so you can map events onto your own records. Omitted when the post was created without it. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

