# Zernio.Model.GetAdAccountBilling200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **string** |  | [optional] 
**PaymentsAccounts** | [**List&lt;GetAdAccountBilling200ResponsePaymentsAccountsInner&gt;**](GetAdAccountBilling200ResponsePaymentsAccountsInner.md) |  | [optional] 
**BillingSetups** | [**List&lt;GetAdAccountBilling200ResponseBillingSetupsInner&gt;**](GetAdAccountBilling200ResponseBillingSetupsInner.md) |  | [optional] 
**AccountBudgets** | [**List&lt;GetAdAccountBilling200ResponseAccountBudgetsInner&gt;**](GetAdAccountBilling200ResponseAccountBudgetsInner.md) |  | [optional] 
**PendingBudgetProposals** | [**List&lt;GetAdAccountBilling200ResponsePendingBudgetProposalsInner&gt;**](GetAdAccountBilling200ResponsePendingBudgetProposalsInner.md) | New account budgets proposed but not yet approved by Google. A setup with one is not reused by the POST. | [optional] 
**CachedAt** | **DateTime?** | When this data was fetched from Google. Null when the cache is unavailable. | [optional] 
**Stale** | **bool** | True when Google&#39;s quota was exhausted and this is the last successful fetch. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

