# Zernio.Model.PortfolioBidStrategy
A Google Ads portfolio bid strategy: a named bidding strategy shared across campaigns, with its R.130 report metrics over the queried date range.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Numeric bid strategy id; pass as portfolioBidStrategyId or in the {strategyId} path. | [optional] 
**Name** | **string** |  | [optional] 
**Type** | **string** |  | [optional] 
**Status** | **string** | ENABLED or REMOVED. | [optional] 
**CampaignCount** | **int** | Number of campaigns currently attached. | [optional] 
**Clicks** | **int** |  | [optional] 
**Cost** | **decimal** | Cost in the account&#39;s currency units (converted from micros). | [optional] 
**CostPerConversion** | **decimal** | Cost per conversion in the account&#39;s currency units. | [optional] 
**Impressions** | **int** |  | [optional] 
**AverageCpc** | **decimal** | Average CPC in the account&#39;s currency units. | [optional] 
**Conversions** | **decimal** |  | [optional] 
**TargetCpa** | **decimal?** | Current target, in the account&#39;s currency units. Null for a ROAS-family type (TARGET_ROAS, MAXIMIZE_CONVERSION_VALUE), or a Maximize type with no target set. Pre-fills the edit form&#39;s target field. | [optional] 
**TargetRoas** | **decimal?** | Current target as a decimal multiplier (2.0 &#x3D; 2.0x). Null for a CPA-family type (TARGET_CPA, MAXIMIZE_CONVERSIONS), or a Maximize type with no target set. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

