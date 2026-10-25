# Zernio.Model.WebhookPayloadAdRuleTriggeredObjectsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PlatformId** | **string** | Platform-native ID of the campaign or ad set. | 
**Name** | **string** | Name on the platform. Falls back to &#x60;platformId&#x60; when the platform reports none. | 
**PlatformCampaignId** | **string** | Platform-native ID of the campaign the object belongs to (on a campaign-level rule, the campaign&#39;s own ID). Null when unknown. | 
**Conditions** | [**List&lt;WebhookPayloadAdRuleTriggeredObjectsInnerConditionsInner&gt;**](WebhookPayloadAdRuleTriggeredObjectsInnerConditionsInner.md) | Every condition of the rule, with the value the object reached. | 
**Actions** | [**List&lt;WebhookPayloadAdRuleTriggeredObjectsInnerActionsInner&gt;**](WebhookPayloadAdRuleTriggeredObjectsInnerActionsInner.md) | What the rule did to the object. Empty on a rule that only notifies. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

