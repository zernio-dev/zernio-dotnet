# Zernio.Model.UpdateAutomationRequestLimits

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Cooldown** | **string** | How long the same post or account is left alone after the automation acts on it, rounded up to whole minutes. None by default. | [optional] 
**MaxChangesPerDay** | **int** | Most runs across the last 24 hours. Required, up to 20, with a boost step. | [optional] 
**MaxChangesPerObject** | **int** | Most times the rule may change one object, over its whole history. Needs an &#x60;ads.*&#x60; step. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

