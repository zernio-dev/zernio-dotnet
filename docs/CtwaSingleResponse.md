# Zernio.Model.CtwaSingleResponse
Response returned by `POST /v1/ads/ctwa` when the request used the single-creative shape (top-level headline / body / imageUrl|video). `adType` is the union discriminator. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdType** | **string** |  | 
**Ad** | **Object** | The persisted Ad document. | 
**Message** | **string** |  | 
**Warnings** | **List&lt;string&gt;** | Present when Meta created the ad set differently from the request: a multi-destination ad set (&#x60;destinations&#x60; including whatsapp) that Meta kept without the requested &#x60;whatsappPhoneNumber&#x60; in its promoted_object, which an existing ad set cannot change (a WhatsApp-only ad set returns no such warning, because every ad routes conversations by the number on its WhatsApp button), or the ad set joined a CBO campaign (&#x60;existingCampaignId&#x60;) whose own bid strategy applies, so a different &#x60;bidStrategy&#x60; or a &#x60;roasAverageFloor&#x60; that strategy cannot take was not applied. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

