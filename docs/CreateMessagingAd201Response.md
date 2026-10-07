# Zernio.Model.CreateMessagingAd201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdType** | **string** |  | 
**Ad** | **Object** | The persisted Ad document. | 
**Message** | **string** |  | 
**Warnings** | **List&lt;string&gt;** | Present when Meta created the ad set differently from the request. Today: Meta kept the ad set without the requested &#x60;whatsappPhoneNumber&#x60; in its promoted_object (the ads still carry it on their WhatsApp button). | [optional] 
**Ads** | **List&lt;Object&gt;** | The persisted Ad documents (one per creative), all sharing the same &#x60;platformCampaignId&#x60; and &#x60;platformAdSetId&#x60;.  | 
**PlatformCampaignId** | **string** |  | 
**PlatformAdSetId** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

