# Zernio.Model.UpdateBidStrategyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Google ads SocialAccount id. | 
**AdAccountId** | **string** | Platform ad account ID (Google customer ID, digits only). Defaults to the account&#39;s connected customer. | [optional] 
**CustomerId** | **string** | Alias of adAccountId, kept for existing callers | [optional] 
**Name** | **string** |  | [optional] 
**Type** | **string** |  | [optional] 
**TargetCpa** | **decimal** |  | [optional] 
**TargetRoas** | **decimal** |  | [optional] 
**TargetImpressionShare** | [**GoogleTargetImpressionShare**](GoogleTargetImpressionShare.md) | Retargets a TARGET_IMPRESSION_SHARE strategy; location, percent and maxCpc are all written. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

