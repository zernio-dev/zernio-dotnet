# Zernio.Model.ListPhoneNumberCountries200ResponseCountriesInnerTypesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**NumberType** | **string** |  | [optional] 
**Tier** | **int?** | Null on a &#x60;fulfilment: request&#x60; type, whose document tier is only known once its requirements are read. | [optional] 
**NeedsKyc** | **bool** |  | [optional] 
**MonthlyCents** | **int** | Price a NEW number of this type costs per month, in cents. | [optional] 
**WhatsappAvailable** | **bool** | Always false for toll_free (WhatsApp does not reliably register toll-free numbers). | [optional] 
**SmsAvailable** | **bool** |  | [optional] 
**CallsAvailable** | **bool** |  | [optional] 
**InStock** | **bool** |  | [optional] 
**Fulfilment** | **string** | &#x60;request&#x60;: the carrier stocks this type nowhere and only sources it to order, so it is always a pre-order. | [optional] 
**PreOrderable** | **bool** | Out of stock but orderable anyway. Submit KYC as usual (POST /v1/phone-numbers/kyc): we buy regular stock the moment it returns, otherwise the carrier sources the number. Usually 2 to 4 weeks, never guaranteed. Only document tiers (3/4) qualify, and nothing is billed until the number is active. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

