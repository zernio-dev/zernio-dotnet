# Zernio.Model.AdRuleRunEvaluationNotification
Set when a run of a rule with a `notify` action matched objects and tried to send the webhook. A notify-only rule whose webhook fails ends with outcome `failed`.  - `done`: the `ad_rule.triggered` webhook is queued for the webhooks subscribed to it (with none subscribed it is still `done`, but nothing is delivered). - `failed`: it could not be queued. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Status** | **string** |  | 
**Reason** | **string** | Why the webhook could not be queued. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

