# Zernio.Model.CreateStandaloneAdRequestCreativesInner
Each creative must supply EXACTLY ONE of `imageUrl` (image creative) or `video` (video creative).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Headline** | **string** |  | 
**Body** | **string** |  | 
**ImageUrl** | **string** | Image creative. Mutually exclusive with &#x60;video&#x60;. | [optional] 
**Video** | [**CreateStandaloneAdRequestCreativesInnerVideo**](CreateStandaloneAdRequestCreativesInnerVideo.md) |  | [optional] 
**LinkUrl** | **string** |  | 
**CallToAction** | **string** |  | 
**LeadGenFormId** | **string** | Per-creative Lead Gen Form ID. Wins over the top-level &#x60;leadGenFormId&#x60; so each ad in a campaign can A/B a different form. Forces CTA to SIGN_UP. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

