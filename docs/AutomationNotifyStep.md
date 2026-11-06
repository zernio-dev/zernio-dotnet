# Zernio.Model.AutomationNotifyStep
Sends a summary to Slack channels or email addresses of connected accounts. In an ad rule it also sends the `ad_rule.triggered` webhook, and `to` is optional.  Event and scheduled automations need `to`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | In an ad rule the id is always &#x60;notify&#x60;. | [optional] 
**Type** | **string** |  | 
**To** | [**List&lt;AutomationNotifyStepToInner&gt;**](AutomationNotifyStepToInner.md) | Up to 5 in an ad rule. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

