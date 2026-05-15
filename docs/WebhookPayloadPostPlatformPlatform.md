# Zernio.Model.WebhookPayloadPostPlatformPlatform
The specific platform that just transitioned to a terminal state.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Platform name (e.g. &#x60;twitter&#x60;, &#x60;tiktok&#x60;, &#x60;instagram&#x60;). | 
**Status** | **string** | Terminal status this event fires on. Matches the event suffix. | 
**PlatformPostId** | **string** | Platform-native post id. Present on &#x60;published&#x60;, absent on &#x60;failed&#x60;. | [optional] 
**PublishedUrl** | **string** | Public URL to the platform-side post. Present on &#x60;published&#x60; (when the platform exposes one and it is not a draft). | [optional] 
**Error** | **string** | Error message from the platform. Present on &#x60;failed&#x60;, absent on &#x60;published&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

