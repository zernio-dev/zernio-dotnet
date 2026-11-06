# Zernio.Model.UpdateAutomationAdAccountControlsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | The ads connection that reaches the ad account. | 
**AdAccountId** | **string** | The platform&#39;s ad account id. | 
**Paused** | **bool** | True stops every automation on this ad account; false lets them run again. | [optional] 
**DailyRaiseLimit** | **decimal?** | The most automations may raise budgets on this ad account in any 24 hours, in the ad account&#39;s currency. A raise past it is cut to the room left.  Send null to remove the limit.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

