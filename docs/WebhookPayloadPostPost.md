# Zernio.Model.WebhookPayloadPostPost

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Content** | **string** | Absent once publishing finishes when the team does not retain content. | [optional] 
**ContentNotRetained** | **bool** | True when this team does not retain content and the post text was already cleared. | [optional] 
**Status** | **string** |  | 
**ScheduledFor** | **DateTime** |  | 
**PublishedAt** | **DateTime** |  | [optional] 
**Platforms** | [**List&lt;WebhookPayloadPostPostPlatformsInner&gt;**](WebhookPayloadPostPostPlatformsInner.md) |  | 
**Metadata** | **Dictionary&lt;string, Object&gt;** | The free-form &#x60;metadata&#x60; object supplied when the post was created, echoed back so you can map events onto your own records. Omitted when the post was created without it. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

