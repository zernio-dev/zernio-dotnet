# Zernio.Model.SocialAccountProfileId

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**UserId** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Description** | **string** |  | [optional] 
**Color** | **string** |  | [optional] 
**Timezone** | **string** | IANA timezone new posts on this profile use when the request names no &#x60;timezone&#x60;. Null means UTC. | [optional] 
**IsDefault** | **bool** |  | [optional] 
**IsOverLimit** | **bool** | Only present when includeOverLimit&#x3D;true. Indicates if this profile exceeds the plan limit. | [optional] 
**AccountCount** | **int** | In the profile list. Connected accounts on the profile, including ones that need reconnecting; phone and SMS number internals and posting accounts hidden by an ads connect are not counted. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

