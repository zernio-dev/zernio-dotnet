# Zernio.Model.ScheduledAutomationDefinitionStepsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Type** | **string** |  | 
**To** | [**List&lt;AutomationNotifyStepToInner&gt;**](AutomationNotifyStepToInner.md) | Up to 5 in an ad rule. | [optional] 
**AdAccountId** | **string** | The Meta ad account that pays, from &#x60;GET /v1/ads/accounts&#x60;. | 
**Budget** | **decimal** | The whole spend of one boost, in the ad account currency. | 
**Days** | **int** | How long each boost runs. | 
**Goal** | **string** |  | [optional] [default to GoalEnum.Engagement]
**Countries** | **List&lt;string&gt;** | ISO 3166 alpha-2 codes. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

