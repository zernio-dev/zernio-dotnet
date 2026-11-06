# Zernio.Model.AutomationAdAccountControls

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | The connection your automations reach the ad account through; null when no automation uses it any more. | 
**Platform** | **string** | The ad platform, for example &#x60;facebook&#x60;. | 
**AdAccountId** | **string** | The platform&#39;s ad account id. | 
**Paused** | **bool** | True when every ad rule on this ad account is stopped. | 
**PausedAt** | **DateTime?** |  | 
**DailyRaiseLimit** | **decimal?** | The most automations may raise budgets on this ad account in any 24 hours, in the ad account&#39;s currency. Null when there is no limit. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

