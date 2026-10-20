# Zernio.Model.CreateGoogleAdAccountRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | 
**AccountId** | **string** | Zernio googleads SocialAccount ID whose Google user reaches the manager. | 
**ManagerCustomerId** | **string** | Manager (MCC) customer id without dashes. The new account is created under it. List reachable managers with GET /v1/ads/accounts/hierarchy. | 
**Name** | **string** | Account name. Whitespace is trimmed. | 
**Currency** | **string** | Uppercase ISO 4217 currency. Cannot be changed after creation. | 
**VarTimeZone** | **string** | IANA time zone name, for example Europe/Madrid. Cannot be changed after creation. | 
**ValidateOnly** | **bool** | Ask Google to validate the request without creating the account. | [optional] [default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

