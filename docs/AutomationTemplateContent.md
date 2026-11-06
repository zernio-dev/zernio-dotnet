# Zernio.Model.AutomationTemplateContent
Where the automations come from. Send `from` or `automations`, not both.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**From** | [**AutomationTemplateContentFrom**](AutomationTemplateContentFrom.md) |  | [optional] 
**Automations** | [**List&lt;AutomationDefinition&gt;**](AutomationDefinition.md) | Automation definitions, each checked like a &#x60;POST /v1/automations&#x60; body. Ad accounts, a trigger&#39;s profile and accounts, and alert destinations become inputs. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

