# Zernio.Model.StartGoogleBusinessVerificationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Method** | **string** | The verification method. Selects which method-specific field below is required. | 
**LanguageCode** | **string** |  | [optional] 
**PhoneNumber** | **string** | For PHONE_CALL / SMS. | [optional] 
**EmailAddress** | **string** | For EMAIL. | [optional] 
**MailerContact** | **Object** | For ADDRESS (postcard) verification. | [optional] 
**Context** | **Object** | ServiceBusinessContext (e.g. service address). Required for service-area businesses. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

