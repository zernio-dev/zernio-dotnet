# Zernio.Model.CreatePhoneNumberPortInRequestEndUser
End-user / current-carrier account info that authorizes the port. The losing carrier matches every field against its records and rejects the whole port on a mismatch — enter values exactly as they appear on the carrier bill. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EntityName** | **string** | Account holder / business name, as on the carrier account. | 
**AuthPersonName** | **string** | Full name (first + last) of the person authorizing the port — must match the LOA signature. | 
**BillingPhoneNumber** | **string** | Phone number on the losing carrier&#39;s bill. Defaults to the ported number itself on single-number orders. Validated as a real phone number when present. | [optional] 
**AccountNumber** | **string** | Account number with the losing carrier — required (carriers reject ports without it; on prepaid mobile plans it is often the phone number itself). | 
**PinPasscode** | **string** | Transfer PIN. Required for mobile numbers (wireless carriers reject PIN-less ports). Forwarded to the carrier, never stored. | [optional] 
**StreetAddress** | **string** |  | 
**ExtendedAddress** | **string** |  | [optional] 
**Locality** | **string** |  | 
**AdministrativeArea** | **string** | 2-letter US state / CA province code (full names are accepted and normalized). | 
**PostalCode** | **string** | US ZIP (5 digits) or Canadian postal code, matching countryCode. | 
**CountryCode** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

