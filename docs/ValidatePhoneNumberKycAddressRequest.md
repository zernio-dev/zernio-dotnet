# Zernio.Model.ValidatePhoneNumberKycAddressRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Country** | **string** | ISO 3166-1 alpha-2 country code. | 
**StreetAddress** | **string** |  | 
**ExtendedAddress** | **string** | Address complement: apartment, suite, unit, or the quadra/lote used in some countries. Optional. Does not substitute for a building number on street_address. | [optional] 
**Locality** | **string** | City / town. | 
**AdministrativeArea** | **string** | State / province / region. When omitted, the pre-check is skipped (the final submit still validates). | [optional] 
**PostalCode** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

