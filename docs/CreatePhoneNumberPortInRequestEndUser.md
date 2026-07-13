# Zernio.Model.CreatePhoneNumberPortInRequestEndUser
End-user / current-carrier account info that authorizes the port.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EntityName** | **string** |  | 
**AuthPersonName** | **string** |  | 
**BillingPhoneNumber** | **string** | Phone number on the losing carrier&#39;s bill. Defaults to the ported number itself on single-number orders. | [optional] 
**AccountNumber** | **string** |  | [optional] 
**PinPasscode** | **string** | Transfer PIN. Forwarded to the carrier, never stored. | [optional] 
**StreetAddress** | **string** |  | 
**ExtendedAddress** | **string** |  | [optional] 
**Locality** | **string** |  | 
**AdministrativeArea** | **string** |  | 
**PostalCode** | **string** |  | 
**CountryCode** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

