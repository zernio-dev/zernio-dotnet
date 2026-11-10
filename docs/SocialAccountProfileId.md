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
**ExternalId** | **string** | Your own identifier for this profile, set on create or update. Null when none is set. | [optional] 
**ContentRetention** | **string** | This profile&#39;s own zero content retention setting. &#x60;none&#x60; stores identifiers and metadata only for this profile. Change it with &#x60;contentRetention&#x60; on update; only the team owner can. | [optional] 
**EffectiveContentRetention** | **string** | The mode that applies to this profile: &#x60;none&#x60; when the profile or the whole team uses zero content retention. | [optional] 
**IsDefault** | **bool** |  | [optional] 
**IsOverLimit** | **bool** | Only present when includeOverLimit&#x3D;true. Indicates if this profile exceeds the plan limit. | [optional] 
**AccountCount** | **int** | In the profile list. Connected accounts on the profile, including ones that need reconnecting; phone and SMS number internals and posting accounts hidden by an ads connect are not counted. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

