# Zernio.Model.CreateBrandedCallingEnterpriseRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**LegalName** | **string** | Exactly as on the tax record. | 
**DoingBusinessAs** | **string** |  | 
**OrganizationType** | **string** |  | 
**OrganizationLegalType** | **string** |  | 
**CountryCode** | **string** | ISO 3166-1 alpha-2. US or CA. | 
**JurisdictionOfIncorporation** | **string** | State, province or country of registration. | 
**Website** | **string** |  | 
**Fein** | **string** | US Federal Employer Identification Number (NN-NNNNNNN) or the Canadian equivalent. Stored encrypted; only the last four digits are ever returned. | 
**Industry** | **string** | One of the carrier industry labels, e.g. technology, healthcare, retail, finance, legal, insurance, real estate, logistics, education. | 
**NumberOfEmployees** | **string** |  | 
**OrganizationContact** | [**BrandedCallingContact**](BrandedCallingContact.md) |  | 
**BillingContact** | [**BrandedCallingContact**](BrandedCallingContact.md) |  | 
**PhysicalAddress** | [**BrandedCallingAddress**](BrandedCallingAddress.md) |  | 
**BillingAddress** | [**BrandedCallingAddress**](BrandedCallingAddress.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

