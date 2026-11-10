# Zernio.Model.UpdateProfileRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | [optional] 
**Description** | **string** | Set to null to clear the description. | [optional] 
**Color** | **string** |  | [optional] 
**Timezone** | **string** | IANA timezone new posts on this profile use when they name no &#x60;timezone&#x60;. Set to null to go back to UTC. An unknown name returns 400. | [optional] 
**ExternalId** | **string** | Your own identifier for this profile (1 to 255 characters, trimmed). Set to null to clear it. A value another profile of the same owner already holds returns 409 profile_external_id_conflict. | [optional] 
**IsDefault** | **bool** |  | [optional] 
**ContentRetention** | **string** | Turns zero content retention on (&#x60;none&#x60;) or off (&#x60;standard&#x60;) for this profile only, for new data within about a minute. Only the team owner can change it. &#x60;standard&#x60; answers 409 while the whole team has it on; &#x60;none&#x60; answers 409 during a WhatsApp verification of a number of this profile. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

