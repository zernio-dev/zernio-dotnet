# Zernio.Model.GetAccountHealth200ResponsePlatformConnection
WhatsApp accounts only. Live probe of the Meta link behind the channel, performed at request time (the same read as GET /v1/whatsapp/number-info).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Status** | **string** | &#x60;connected&#x60; &#x3D; Meta served the channel object. &#x60;disconnected&#x60; &#x3D; Meta refused to serve it (Graph error 100, subcode 33), which is how a phone-side coexistence disconnect surfaces. &#x60;unknown&#x60; &#x3D; the live read failed for another reason (timeout, transient Meta error), not evidence either way. | [optional] 
**CheckedAt** | **DateTime** | When this live probe ran (always the current request; never cached) | [optional] 
**PhoneStatus** | **string** | Meta&#39;s own &#x60;status&#x60; field from the phone-number node (for example CONNECTED), when the object was readable | [optional] 
**MetaError** | [**GetAccountHealth200ResponsePlatformConnectionMetaError**](GetAccountHealth200ResponsePlatformConnectionMetaError.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

