# Zernio.Model.ListPhoneNumberCountries200ResponseCountriesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **string** | ISO 3166-1 alpha-2 | [optional] 
**Tier** | **int** |  | [optional] 
**MonthlyCents** | **int** |  | [optional] 
**NeedsKyc** | **bool** |  | [optional] 
**CallsAvailable** | **bool** | Regular phone (PSTN) calling on the number, inbound + outbound. Available on every offerable country. | [optional] 
**WhatsappAvailable** | **bool** | WhatsApp can be enabled on numbers from this country. | [optional] 
**SmsAvailable** | **bool** | Whether this country&#39;s number type can do SMS. Use it to filter the picker when the buyer wants SMS (pair with &#x60;wantsSms&#x60; on purchase). | [optional] 
**OutboundCallingAvailable** | **bool** | WhatsApp Business Calling (BIC) outbound availability, a Meta feature blocked in some countries. NOT the PSTN Calls feature (&#x60;callsAvailable&#x60;). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

