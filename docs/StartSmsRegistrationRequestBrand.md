# Zernio.Model.StartSmsRegistrationRequestBrand
Required for 10DLC. The legal entity behind the traffic (TCR brand).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EntityType** | **string** |  | 
**DisplayName** | **string** |  | 
**CompanyName** | **string** | Legal company name. Required for every entityType except SOLE_PROPRIETOR. | [optional] 
**Ein** | **string** | Required for every entityType except SOLE_PROPRIETOR. | [optional] 
**Phone** | **string** | Business contact phone. Required for every entityType except SOLE_PROPRIETOR. | [optional] 
**MobilePhone** | **string** | Required for SOLE_PROPRIETOR; the verification OTP is texted there (US/CA mobile). | [optional] 
**Street** | **string** |  | 
**City** | **string** |  | 
**State** | **string** |  | 
**PostalCode** | **string** |  | 
**Country** | **string** | ISO 3166-1 alpha-2 country where the company is registered. Companies worldwide can register standard 10DLC (non-US companies use their local tax ID in &#x60;ein&#x60;; carrier vetting may take longer). SOLE_PROPRIETOR is US/CA only. | 
**Email** | **string** | Brand contact email; defaults to your account email when omitted. | [optional] 
**Website** | **string** | The brand&#39;s website (sole proprietors may use a social profile such as LinkedIn or a business Facebook page). Carriers verify the brand against it; a bare domain is normalized to https://. | 
**Vertical** | **string** |  | 
**StockSymbol** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

