# Zernio.Model.AutomationControls
The team's switch for every ad rule, and each ad account's own controls. Every team member sees the same ones.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Paused** | **bool** | True when every ad rule of the team is stopped. Each rule keeps its own status. | 
**PausedAt** | **DateTime?** | When the team switch was turned off; null while it is on. | 
**AdAccounts** | [**List&lt;AutomationAdAccountControls&gt;**](AutomationAdAccountControls.md) | Every ad account your automations use, plus any ad account that has controls set. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

