# Zernio.Model.EnableSmsOnNumber200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Enabled** | **bool** |  | [optional] 
**Id** | **string** | The SMS social account ID (present when enabled). | [optional] 
**PhoneNumber** | **string** |  | [optional] 
**IsActive** | **bool** | False for US numbers until their registration is approved. | [optional] 
**Country** | **string** |  | [optional] 
**SmsCapable** | **bool?** | Null when capability can&#39;t be read yet (still provisioning). | [optional] 
**MmsCapable** | **bool** |  | [optional] 
**DomesticOnly** | **bool** |  | [optional] 
**NotReady** | **bool** | Number is still provisioning at the carrier; retry shortly. | [optional] 
**NeedsRegistration** | **bool** | US only; a carrier registration is required before delivery. | [optional] 
**AlreadyRegistered** | **bool** | A prior non-rejected registration already covers this number; no re-submit needed. | [optional] 
**RegistrationStatus** | **string** |  | [optional] 
**Reusable** | [**EnableSmsOnNumber200ResponseReusable**](EnableSmsOnNumber200ResponseReusable.md) |  | [optional] 
**Message** | **string** | Human-readable explanation when &#x60;enabled&#x60; is false. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

