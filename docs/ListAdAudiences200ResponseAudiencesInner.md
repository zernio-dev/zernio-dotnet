# Zernio.Model.ListAdAudiences200ResponseAudiencesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The Zernio audience id. Pass this as audienceId on GET /v1/ads/audiences/{audienceId} and the companies/users upload endpoints. Null when the audience was not created through Zernio. | [optional] 
**AccountId** | **string** | Account the audience was created against. Returned for saved_targeting items. | [optional] 
**PlatformAudienceId** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Description** | **string** |  | [optional] 
**Type** | **string** |  | [optional] 
**Spec** | [**TargetingSpec**](TargetingSpec.md) |  | [optional] 
**Platform** | **string** |  | [optional] 
**Size** | **int** |  | [optional] 
**Status** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

