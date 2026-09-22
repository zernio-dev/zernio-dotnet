# Zernio.Model.CreateBidStrategyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Google ads SocialAccount id. | 
**AdAccountId** | **string** | Platform ad account ID (Google customer ID, digits only). Defaults to the account&#39;s connected customer. | [optional] 
**CustomerId** | **string** | Alias of adAccountId, kept for existing callers | [optional] 
**Name** | **string** |  | 
**Type** | **string** |  | 
**TargetCpa** | **decimal** | Required when type is TARGET_CPA, in the account&#39;s currency units. | [optional] 
**TargetRoas** | **decimal** | Required when type is TARGET_ROAS; a multiplier (2.0 &#x3D; 2.0x). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

