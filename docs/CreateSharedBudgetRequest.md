# Zernio.Model.CreateSharedBudgetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Google ads SocialAccount id. | 
**AdAccountId** | **string** | Platform ad account ID (Google customer ID, digits only). Defaults to the account&#39;s connected customer. | [optional] 
**Name** | **string** |  | 
**Amount** | **decimal** | Daily amount in the account&#39;s currency units. | 
**Type** | **string** | Only daily is accepted (lifetime returns 422). | [optional] [default to TypeEnum.Daily]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

