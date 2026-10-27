# Zernio.Model.ListAdAudiences200ResponseAudiencesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The Zernio audience id. Pass this as audienceId on GET /v1/ads/audiences/{audienceId} and the companies/users upload endpoints. Null when the audience was not created through Zernio. | [optional] 
**AccountId** | **string** | Account the audience was created against. Returned for saved_targeting items. | [optional] 
**PlatformAudienceId** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Description** | **string** |  | [optional] 
**Type** | **string** | &#x60;reddit_engagement&#x60;, &#x60;third_party&#x60; and &#x60;in_market&#x60; are listed from Reddit (engagement retargeting, and Reddit&#39;s own audiences) so they can be targeted. Zernio cannot create them. | [optional] 
**Spec** | [**TargetingSpec**](TargetingSpec.md) |  | [optional] 
**Platform** | **string** |  | [optional] 
**Size** | **int** |  | [optional] 
**Status** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

