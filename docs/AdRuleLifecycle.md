# Zernio.Model.AdRuleLifecycle
Turns matches into alerts. An object acts and notifies only after `confirmChecks` matching runs in a row; its alert stays open while it matches or `hold` holds, and resolves on its own (a day after the object stops delivering). Cooldown and caps still decide repeat actions.  The alert is critical while `critical` holds and goes back to warning when it stops, with no webhook. `escalated` is sent once per alert.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ConfirmChecks** | **int** | Matching runs in a row before acting. Defaults to 1. | [optional] 
**Hold** | [**AdRuleConditions**](AdRuleConditions.md) | Keeps an open alert open after the conditions stop matching. | [optional] 
**Critical** | [**AdRuleConditions**](AdRuleConditions.md) | Marks an open alert critical. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

