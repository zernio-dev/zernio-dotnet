# Zernio.Model.SetUpAdAccountBillingRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to store this write as a staged change instead of applying it. The response is &#x60;202&#x60; with the change, and POST /v1/ads/changes/{changeId}/confirm applies it later. Cannot be combined with &#x60;validateOnly&#x60;. | [optional] 
**AccountId** | **string** | Google ads SocialAccount id. | 
**AdAccountId** | **string** | Google Ads customer id to bill, digits only. | 
**PaymentsAccountId** | **string** | Monthly invoicing payments account from GET /v1/ads/accounts/billing. | 
**SpendingLimit** | **decimal** | Account budget cap in the account currency. Omit for an unlimited budget. | [optional] 
**BudgetName** | **string** |  | [optional] [default to "Zernio account budget"]
**PurchaseOrderNumber** | **string** | Printed on the invoice. No effect on delivery. | [optional] 
**ValidateOnly** | **bool** |  | [optional] [default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

