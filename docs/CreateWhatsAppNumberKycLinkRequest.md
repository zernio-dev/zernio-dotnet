# Zernio.Model.CreateWhatsAppNumberKycLinkRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** |  | 
**Country** | **string** | ISO 3166-1 alpha-2 country code (must be a regulated/KYC country). | 
**Branding** | [**CreateWhatsAppNumberKycLinkRequestBranding**](CreateWhatsAppNumberKycLinkRequestBranding.md) |  | [optional] 
**RedirectUrl** | **string** | Where to send the end customer&#39;s browser after a successful submit. On completion Zernio appends &#x60;kyc&#x3D;submitted&#x60; and &#x60;country&#x3D;&lt;ISO-2&gt;&#x60; as query params. When omitted, the hosted page shows a built-in confirmation screen instead.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

