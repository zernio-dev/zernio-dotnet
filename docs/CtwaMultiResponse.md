# Zernio.Model.CtwaMultiResponse
Response returned by `POST /v1/ads/ctwa` when the request used the multi-creative shape (`creatives[]`). N persisted Ad documents share the returned `platformCampaignId` and `platformAdSetId`. `adType` is the union discriminator. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdType** | **string** |  | 
**Ads** | **List&lt;Object&gt;** | The persisted Ad documents (one per creative), all sharing the same &#x60;platformCampaignId&#x60; and &#x60;platformAdSetId&#x60;.  | 
**PlatformCampaignId** | **string** |  | 
**PlatformAdSetId** | **string** |  | 
**Message** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

