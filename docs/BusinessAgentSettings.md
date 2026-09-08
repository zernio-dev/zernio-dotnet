# Zernio.Model.BusinessAgentSettings
Meta Business Agent settings for one WhatsApp number, as Meta returns them.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AgentId** | **string** |  | 
**Channel** | **string** |  | 
**Rollout** | [**BusinessAgentSettingsRollout**](BusinessAgentSettingsRollout.md) |  | 
**Handoff** | [**BusinessAgentSettingsHandoff**](BusinessAgentSettingsHandoff.md) |  | [optional] 
**Followup** | [**BusinessAgentSettingsFollowup**](BusinessAgentSettingsFollowup.md) |  | [optional] 
**AiAudience** | **string** | EVERYONE answers all consumers; ALLOWLISTED_ONLY answers only the allowlist and needs no payment method. | [optional] 
**NeverSayPhrases** | **List&lt;string&gt;** | Exact phrases the agent must never say. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

