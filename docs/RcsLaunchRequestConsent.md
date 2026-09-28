# Zernio.Model.RcsLaunchRequestConsent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**OptInMethods** | [**List&lt;RcsLaunchRequestConsentOptInMethodsInner&gt;**](RcsLaunchRequestConsentOptInMethodsInner.md) |  | 
**CallToAction** | **string** | The opt-in wording people agree to. | 
**CallToActionUrl** | **string** | Required for WEBSITE opt-in. | [optional] 
**CallToActionMediaUrl** | **string** | Screenshot of the opt-in. Required for WEBSITE and MOBILE_APP opt-in. | [optional] 
**DoubleOptIn** | **bool** |  | 
**DoubleOptInMessage** | **string** | Required when doubleOptIn is true. | [optional] 
**OptInMessage** | **string** |  | 
**HelpResponse** | **string** |  | 
**OptOutResponse** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

