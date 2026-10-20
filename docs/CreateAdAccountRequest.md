# Zernio.Model.CreateAdAccountRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | 
**AccountId** | **string** | Zernio googleads SocialAccount ID whose Google user reaches the manager. | 
**BusinessId** | **string** | Business portfolio that will own the account. | 
**Name** | **string** | Account name. Whitespace is trimmed. | 
**Currency** | **string** | Uppercase ISO 4217 currency. Cannot be changed after creation. | 
**TimezoneId** | **long** | Numeric Meta timezone ID from the linked timezone list. For example 1 is America/Los_Angeles. | 
**EndAdvertiser** | **string** | End advertiser business or page ID. NONE uses the owning business. | [optional] [default to "NONE"]
**MediaAgency** | **string** | Media agency business or page ID. NONE for self-serve customers. | [optional] [default to "NONE"]
**Partner** | **string** | Partner business or page ID. NONE for self-serve customers. | [optional] [default to "NONE"]
**Invoice** | **bool** | Request Meta invoicing. Eligibility is determined by Meta. | [optional] 
**InvoiceGroupId** | **string** | Existing Meta invoice group ID. | [optional] 
**InvoicingEmails** | **List&lt;string&gt;** | Addresses for Meta invoices. | [optional] 
**Io** | **bool** | Meta insertion-order invoicing option. | [optional] 
**PoNumber** | **string** | Purchase order number. | [optional] 
**FundingId** | **string** | Existing Meta funding reference. Does not add a payment method. | [optional] 
**AdAccountCreatedFromBmFlag** | **bool** | Meta Business Manager creation flag. | [optional] 
**ManagerCustomerId** | **string** | Manager (MCC) customer id without dashes. The new account is created under it. List reachable managers with GET /v1/ads/accounts/hierarchy. | 
**VarTimeZone** | **string** | IANA time zone name, for example Europe/Madrid. Cannot be changed after creation. | 
**ValidateOnly** | **bool** | Ask Google to validate the request without creating the account. | [optional] [default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

