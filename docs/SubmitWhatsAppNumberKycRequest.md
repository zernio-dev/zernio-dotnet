# Zernio.Model.SubmitWhatsAppNumberKycRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** |  | 
**Country** | **string** |  | 
**Reuse** | **bool** | Reuse a prior approved verification for this country (skips document/field collection; places the order immediately). | [optional] 
**EndUserFirstName** | **string** | End user&#39;s legal first name. Required when the country has an action/ID-verification (Onfido) requirement. | [optional] 
**EndUserLastName** | **string** | End user&#39;s legal last name. Same condition as endUserFirstName. | [optional] 
**Values** | **Dictionary&lt;string, string&gt;** | requirementId → textual value | [optional] 
**Documents** | [**List&lt;SubmitWhatsAppNumberKycRequestDocumentsInner&gt;**](SubmitWhatsAppNumberKycRequestDocumentsInner.md) |  | [optional] 
**Address** | [**SubmitWhatsAppNumberKycRequestAddress**](SubmitWhatsAppNumberKycRequestAddress.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

