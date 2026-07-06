# Zernio.Model.StartSmsRegistrationRequestBrand
Required for 10DLC. The legal entity behind the traffic (TCR brand).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EntityType** | **string** |  | 
**DisplayName** | **string** |  | 
**CompanyName** | **string** | Legal company name. Required for every entityType except SOLE_PROPRIETOR. | [optional] 
**Ein** | **string** | Required for every entityType except SOLE_PROPRIETOR. | [optional] 
**Phone** | **string** |  | [optional] 
**MobilePhone** | **string** | Required for SOLE_PROPRIETOR; the verification OTP is texted there (US/CA mobile). | [optional] 
**Street** | **string** |  | [optional] 
**City** | **string** |  | [optional] 
**State** | **string** |  | [optional] 
**PostalCode** | **string** |  | [optional] 
**Country** | **string** |  | 
**Email** | **string** | Brand contact email; defaults to your account email when omitted. | [optional] 
**Website** | **string** |  | [optional] 
**Vertical** | **string** |  | 
**StockSymbol** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

