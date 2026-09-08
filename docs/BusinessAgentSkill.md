# Zernio.Model.BusinessAgentSkill

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Title** | **string** | Lowercase letters, digits and hyphens, e.g. greeting-skill. | [optional] 
**Description** | **string** | When the agent should apply the skill. | [optional] 
**Skill** | **string** | The instructions themselves. Avoid two skills that both claim priority for the same situation. | 
**Id** | **string** |  | 
**Channel** | **string** |  | [optional] 
**CreatedAt** | **int** | Unix seconds. | [optional] 
**Status** | **string** | pending_review right after a write; blocked means Meta content review rejected it and the agent never applies it. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

