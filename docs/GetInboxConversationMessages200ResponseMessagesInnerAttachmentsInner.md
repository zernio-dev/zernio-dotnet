# Zernio.Model.GetInboxConversationMessages200ResponseMessagesInnerAttachmentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Type** | **string** |  | [optional] 
**Url** | **string** | Direct media link. On Instagram and Facebook this is a signed Meta CDN url that EXPIRES: use it now, do not store it. Persist &#x60;refreshUrl&#x60; instead. | [optional] 
**RefreshUrl** | **string** | Instagram and Facebook only. Endpoint that resolves this attachment to a working url every time, re-minting it from Meta when the stored one has expired. Safe to store and render indefinitely. | [optional] 
**Filename** | **string** |  | [optional] 
**PreviewUrl** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

