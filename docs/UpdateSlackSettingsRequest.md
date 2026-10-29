# Zernio.Model.UpdateSlackSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DefaultUsername** | **string** | Author name shown on posts. Empty string clears it. | [optional] 
**DefaultIconUrl** | **string** | Author avatar image URL. Empty string clears it. | [optional] 
**ApplyToWorkspace** | **bool** | Applies the name and icon to every connected channel of this Slack workspace owned by the same owner, on the same Slack app, in profiles the caller can access. Channels connected later inherit the identity from a channel of that workspace. | [optional] [default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

