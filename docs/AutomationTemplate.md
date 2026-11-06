# Zernio.Model.AutomationTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | A team template&#39;s id (24 hex characters), or the id of one of Zernio&#39;s templates such as &#x60;stop_losers&#x60;. | 
**Name** | **string** |  | 
**Description** | **string** |  | 
**Publisher** | [**AutomationTemplatePublisher**](AutomationTemplatePublisher.md) |  | 
**Visibility** | **string** | &#x60;team&#x60;: your team only. &#x60;link&#x60;: anyone with the share link can read and install it. &#x60;public&#x60;: one of Zernio&#39;s templates. | 
**VarVersion** | **int** | Goes up each time the content changes. Renaming or sharing keeps it. | 
**Areas** | **List&lt;AutomationTemplate.AreasEnum&gt;** | What its automations work on. | 
**Inputs** | [**List&lt;AutomationTemplateInput&gt;**](AutomationTemplateInput.md) |  | 
**Automations** | [**List&lt;AutomationTemplateAutomation&gt;**](AutomationTemplateAutomation.md) |  | 
**Installs** | **int** | Installs across every team. Always 0 on Zernio&#39;s templates. | 
**InstalledInTeam** | **int** | Your team&#39;s automations made from it. Absent on shared and Zernio templates. | [optional] 
**Share** | [**AutomationTemplateShare**](AutomationTemplateShare.md) |  | 
**CreatedBy** | **string** | The user who saved it. Only on your team&#39;s templates. | [optional] 
**CreatedAt** | **DateTime** | Absent on Zernio&#39;s templates. | [optional] 
**UpdatedAt** | **DateTime** | Absent on Zernio&#39;s templates. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

