# Zernio.Model.WebhookPayloadAdVideoProcessedVideo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Meta video id, as returned by the 202 upload response. | 
**PlatformAdAccountId** | **string** | Meta ad account id (act_&lt;n&gt;) the video was uploaded to. | 
**Status** | **string** | &#x60;ready&#x60;: usable as &#x60;video.id&#x60; on the create endpoints. &#x60;error&#x60;: Meta could not process it; upload again. | 
**Error** | **string** | Meta&#39;s processing error when status is &#x60;error&#x60;, otherwise null. | 
**ThumbnailUrl** | **string** | Meta&#39;s auto-generated poster when status is &#x60;ready&#x60; and Meta produced one, otherwise null. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

