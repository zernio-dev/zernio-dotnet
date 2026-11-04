# Zernio.Model.WebhookPayloadAutomationActionAction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**SubjectId** | **string** | The platform&#39;s id of the object changed: an ad, ad set or campaign for ad rules. | 
**Type** | **string** | &#x60;pause&#x60;, &#x60;activate&#x60;, &#x60;adjust_budget&#x60; or &#x60;notify&#x60; for ad rules. New values may be added. | 
**Status** | **string** |  | 
**Reason** | **string** |  | 
**Previous** | **Dictionary&lt;string, Object&gt;** | The value before the change, such as &#x60;{ \&quot;dailyBudget\&quot;: 40 }&#x60;. | 
**Target** | **Dictionary&lt;string, Object&gt;** | The value the change sets, such as &#x60;{ \&quot;dailyBudget\&quot;: 48 }&#x60; or &#x60;{ \&quot;status\&quot;: \&quot;paused\&quot; }&#x60;. | 
**ActedAt** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

