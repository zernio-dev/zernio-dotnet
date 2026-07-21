# Zernio.Model.GetAdAccountFinance200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdAccountId** | **string** |  | [optional] 
**Currency** | **string** | ISO 4217 code all money values are expressed in. | [optional] 
**Balance** | **decimal** | Outstanding/prepaid balance in whole currency units. | [optional] 
**AmountSpent** | **decimal** | Lifetime amount spent in whole currency units. | [optional] 
**SpendCap** | **decimal?** | Account spend cap; null when none is set. | [optional] 
**FundingSource** | [**GetAdAccountFinance200ResponseFundingSource**](GetAdAccountFinance200ResponseFundingSource.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

