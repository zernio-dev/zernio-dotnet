# Zernio.Model.AutomationAlert
Turns matches into alerts: the ad rule acts only after `confirmChecks` matching checks in a row, keeps the alert open while `hold` holds and marks it critical when `critical` holds.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ConfirmChecks** | **int** |  | [optional] 
**Hold** | [**AdRuleConditions**](AdRuleConditions.md) |  | [optional] 
**Critical** | [**AdRuleConditions**](AdRuleConditions.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

