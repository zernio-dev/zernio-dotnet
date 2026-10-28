# Zernio.Model.TrackingWindow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**PostId** | **string** | The external post being tracked | 
**AccountId** | **string** |  | 
**Platform** | **string** |  | 
**PlatformPostId** | **string** | The post&#39;s id on the platform | 
**StartsAt** | **DateTime** |  | 
**EndsAt** | **DateTime** |  | 
**Status** | **string** |  | 
**FinalReadAt** | **DateTime?** | When the closing read ran. Null until then. | 
**CompletionReason** | **string** | How the window closed. Null while it is open. | 
**RequestedBy** | **string** |  | 
**Latest** | [**TrackingWindowLatest**](TrackingWindowLatest.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

