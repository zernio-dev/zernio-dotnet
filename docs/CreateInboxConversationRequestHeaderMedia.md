# Zernio.Model.CreateInboxConversationRequestHeaderMedia
WhatsApp only. Overrides a media-header template's header asset for THIS send, so a template with an image/video/document header can carry a different asset per message (e.g. each recipient their own invoice PDF). Without it, the template's approved sample asset is sent. Provide exactly one of link or id.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** | Must match the template header&#39;s media type. | 
**Link** | **string** | Public URL of the asset to send. Must be reachable without auth. | [optional] 
**Id** | **string** | A Meta media id (from the media upload endpoint), as an alternative to link. | [optional] 
**Filename** | **string** | Document display name shown to the recipient (e.g. \&quot;Factura 0001-123.pdf\&quot;). document type only; ignored for image/video. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

