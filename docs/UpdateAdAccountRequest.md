# Zernio.Model.UpdateAdAccountRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Account ID (metaads, or a facebook/instagram posting account) | 
**AdAccountId** | **string** | Meta ad account ID (act_...) | 
**Name** | **string** | New ad account name. | [optional] 
**SpendCap** | **decimal?** | Account spend cap in whole currency units; null removes it. | [optional] 
**ResetAmountSpent** | **bool** | Restart the amount counted against the cap from zero. Cannot be combined with spendCap null. | [optional] 
**DefaultDsaBeneficiary** | **string** | Legal entity benefiting from ads on this ad account | [optional] 
**DefaultDsaPayor** | **string** | Legal entity paying for ads on this ad account. Defaults to defaultDsaBeneficiary when omitted. Requires defaultDsaBeneficiary. | [optional] 
**TrackingUrlTemplate** | **string** | **Google only.** Account tracking template (customer.tracking_url_template); an empty string clears it. | [optional] 
**FinalUrlSuffix** | **string** | **Google only.** Account final URL suffix (customer.final_url_suffix); an empty string clears it. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

