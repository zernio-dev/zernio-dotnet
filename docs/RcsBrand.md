# Zernio.Model.RcsBrand

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DisplayName** | **string** |  | 
**LegalName** | **string** | Exactly as on IRS records. | 
**LegalEntityType** | **string** |  | 
**OrganizationType** | **string** |  | 
**WebsiteUrl** | **string** |  | 
**TaxId** | **string** | US: the EIN, 9 digits, optionally NN-NNNNNNN. Elsewhere: the national tax or company registration id. | 
**StockSymbol** | **string** | EXCHANGE:SYMBOL. Required for PUBLIC_PROFIT. | [optional] 
**Address** | [**RcsBrandInputAddress**](RcsBrandInputAddress.md) |  | 
**Contact** | [**RcsBrandInputContact**](RcsBrandInputContact.md) |  | 
**Id** | **string** |  | [optional] 
**Status** | **string** | draft &#x3D; not filed yet (still editable). | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

