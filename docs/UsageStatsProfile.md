# Zernio.Model.UsageStatsProfile
Present with `profileId` / `externalId` on `GET /v1/usage-stats`: the per-profile counters. Everything outside this block stays team-level.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** |  | 
**ExternalId** | **string** | The externalId set on the profile, null when it has none. | 
**Usage** | [**UsageStatsProfileAllOfUsage**](UsageStatsProfileAllOfUsage.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

