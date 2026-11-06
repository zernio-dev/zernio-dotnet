# Zernio.Model.AutomationTemplateInput
Something an install asks for. Each automation in the template holds `{ \"$input\": \"<key>\" }` where the value goes, and installing puts the value sent in `inputs.<key>` there.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Key** | **string** | The name to send the value under in &#x60;inputs&#x60;, for example &#x60;adAccount&#x60;. | 
**Type** | **string** | What the value is. &#x60;ad_account&#x60;: &#x60;{ accountId, adAccountId }&#x60;. &#x60;profile&#x60;: a profile id. &#x60;social_accounts&#x60;: an array of social account ids. &#x60;notify_destination&#x60;: an array of &#x60;{ accountId, to?, channelId? }&#x60;. &#x60;number&#x60;, &#x60;money&#x60; (in the ad account&#39;s currency) and &#x60;percent&#x60;: a number within the bounds below. &#x60;choice&#x60;: one of &#x60;options[].value&#x60;. | 
**Label** | **string** |  | 
**Optional** | **bool** | True when an install may leave it out. A field that points at a left-out input is dropped. | [optional] 
**Default** | [**AutomationTemplateInputDefault**](AutomationTemplateInputDefault.md) |  | [optional] 
**Min** | **decimal** |  | [optional] 
**ExclusiveMin** | **decimal** | The value must be above it, for example an amount above 0. | [optional] 
**Max** | **decimal** |  | [optional] 
**Integer** | **bool** | True when only whole numbers are accepted. | [optional] 
**Options** | [**List&lt;AutomationTemplateInputOptionsInner&gt;**](AutomationTemplateInputOptionsInner.md) | What a &#x60;choice&#x60; input offers. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

