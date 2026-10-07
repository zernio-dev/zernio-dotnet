# Zernio.Model.CtwaSingleResponse
Response returned by `POST /v1/ads/ctwa` when the request used the single-creative shape (top-level headline / body / imageUrl|video). `adType` is the union discriminator. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdType** | **string** |  | 
**Ad** | **Object** | The persisted Ad document. | 
**Message** | **string** |  | 
**Warnings** | **List&lt;string&gt;** | Present when Meta created the ad set differently from the request. Today: Meta kept the ad set without the requested &#x60;whatsappPhoneNumber&#x60; in its promoted_object (the ads still carry it on their WhatsApp button). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

