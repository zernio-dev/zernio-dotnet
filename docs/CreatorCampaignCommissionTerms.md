# Zernio.Model.CreatorCampaignCommissionTerms
Commission on store orders. Set `percentOfSalesBps`, `perOrderCents` or both. Sales are the line items after discounts, before shipping and tax; refunds come off them, and a cancelled or fully refunded order earns nothing.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PercentOfSalesBps** | **int** | Share of the sales in basis points: 1500 is 15%. | [optional] 
**PerOrderCents** | **int** | A flat amount per credited order. | [optional] 
**Attribution** | **string** | How an order is credited: the creator&#39;s discount code, the last click on their tracking link, or both with the code winning. | [optional] [default to AttributionEnum.CodeOrLink]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

