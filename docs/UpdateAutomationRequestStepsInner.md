# Zernio.Model.UpdateAutomationRequestStepsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Type** | **string** |  | 
**IncludeManuallyPaused** | **bool** | Also objects a person paused. Without it only what this automation paused is turned back on. | [optional] 
**Status** | **string** | The copy starts paused unless &#x60;active&#x60;. | [optional] 
**RenameSuffix** | **string** |  | [optional] 
**By** | **string** | From 1% to 90%. | 
**Max** | **decimal** | A receiver&#39;s budget never goes above this. | [optional] 
**Min** | **decimal** | A giver&#39;s budget never goes below this. | [optional] 
**Amount** | **decimal** |  | 
**Target** | **string** |  | 
**Metric** | **string** | A condition metric or &#x60;result:&lt;key&gt;&#x60;, not a calendar metric. | 
**Window** | **string** | A condition window. | 
**Best** | **string** | Which end is best. Defaults to lowest for &#x60;cpa&#x60;, &#x60;cpc&#x60;, &#x60;cpm&#x60;, &#x60;frequency&#x60; and cost results, highest otherwise. | [optional] 
**From** | **int** | How many objects give budget. | 
**To** | [**List&lt;AutomationNotifyStepToInner&gt;**](AutomationNotifyStepToInner.md) | Up to 5 in an ad rule. | 
**Add** | **string** |  | [optional] 
**Remove** | **string** |  | [optional] 
**At** | **string** |  | [optional] 
**ExpiresIn** | **string** | From &#x60;15m&#x60; to &#x60;7d&#x60;, in whole minutes. | 
**AdAccountId** | **string** | The Meta ad account that pays, from &#x60;GET /v1/ads/accounts&#x60;. | 
**Budget** | **decimal** | The whole spend of one boost, in the ad account currency. | 
**Days** | **int** | How long each boost runs. | 
**Goal** | **string** |  | [optional] [default to GoalEnum.Engagement]
**Countries** | **List&lt;string&gt;** | ISO 3166 alpha-2 codes. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

