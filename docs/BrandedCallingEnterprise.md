# Zernio.Model.BrandedCallingEnterprise

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**LegalName** | **string** |  | [optional] 
**DoingBusinessAs** | **string** |  | [optional] 
**OrganizationType** | **string** |  | [optional] 
**OrganizationLegalType** | **string** |  | [optional] 
**CountryCode** | **string** |  | [optional] 
**JurisdictionOfIncorporation** | **string** |  | [optional] 
**Website** | **string** |  | [optional] 
**FeinLast4** | **string** | Last four digits of the tax id; the full id is never returned. | [optional] 
**Industry** | **string** |  | [optional] 
**NumberOfEmployees** | **string** |  | [optional] 
**OrganizationContact** | [**BrandedCallingContact**](BrandedCallingContact.md) |  | [optional] 
**BillingContact** | [**BrandedCallingContact**](BrandedCallingContact.md) |  | [optional] 
**PhysicalAddress** | [**BrandedCallingAddress**](BrandedCallingAddress.md) |  | [optional] 
**BillingAddress** | [**BrandedCallingAddress**](BrandedCallingAddress.md) |  | [optional] 
**Registered** | **bool** | True once the business exists at the carrier (happens when its first identity passes review). | [optional] 
**CreatedAt** | **DateTime?** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

