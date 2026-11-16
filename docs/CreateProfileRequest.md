# Zernio.Model.CreateProfileRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Description** | **string** |  | [optional] 
**Color** | **string** |  | [optional] 
**Timezone** | **string** | IANA timezone new posts on this profile use when they name no &#x60;timezone&#x60;. Omit to keep UTC. An unknown name returns 400. | [optional] 
**ExternalId** | **string** | Your own identifier for this profile, typically the id of the tenant or client it serves in your system (1 to 255 characters, trimmed). Unique among the profiles of the user who owns the profile: a duplicate returns 409 profile_external_id_conflict. Look a profile up by it with GET /v1/profiles?externalId&#x3D;. | [optional] 
**ContentRetention** | **string** | Set &#x60;none&#x60; to create the profile with zero content retention, so nothing of its accounts is stored from the first sync. Only the team owner can, with a session or a full-access key; anyone else gets 403. | [optional] 
**MaxOutboundCallsPerHour** | **int** | Caps outbound calls from this profile&#39;s numbers per rolling hour, inside the team limits. Omit for no profile cap. | [optional] 
**MaxDailyCallSpendUsd** | **decimal** | Caps billed call spend (USD) from this profile&#39;s numbers per rolling 24 hours, inside the team limits. Omit for no profile cap. | [optional] 
**MaxForwardedMinutesPerDay** | **int** | Caps minutes forwarded to a phone from this profile&#39;s numbers per rolling 24 hours, inside the team limits. Omit for no profile cap. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

