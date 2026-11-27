# Zernio.Model.CreateBidStrategyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to store this write as a staged change instead of applying it. The response is &#x60;202&#x60; with the change, and POST /v1/ads/changes/{changeId}/confirm applies it later. Cannot be combined with &#x60;validateOnly&#x60;. | [optional] 
**AccountId** | **string** | Google ads SocialAccount id. | 
**AdAccountId** | **string** | Platform ad account ID (Google customer ID, digits only). Defaults to the account&#39;s connected customer. | [optional] 
**CustomerId** | **string** | Alias of adAccountId, kept for existing callers | [optional] 
**Name** | **string** |  | 
**Type** | **string** |  | 
**TargetCpa** | **decimal** | Required when type is TARGET_CPA, in the account&#39;s currency units. | [optional] 
**TargetRoas** | **decimal** | Required when type is TARGET_ROAS; a multiplier (2.0 &#x3D; 2.0x). | [optional] 
**TargetImpressionShare** | [**GoogleTargetImpressionShare**](GoogleTargetImpressionShare.md) | Required when type is TARGET_IMPRESSION_SHARE, and refused with any other type. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

