# Zernio.Model.HubSpotSettingsSyncIssue
Set while the portal refuses to create contacts because it requires properties Zernio does not fill. People already in HubSpot are still matched and their messages logged. Cleared by the next created contact or a change to `contactDefaults`. The account's health shows it too.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **string** |  | 
**Properties** | **List&lt;string&gt;** | The required contact properties HubSpot named. | 
**Message** | **string** |  | 
**At** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

