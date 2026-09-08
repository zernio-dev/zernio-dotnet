# Zernio.Model.BusinessAgentStatus
Where the merchant is in the Meta Business Agent setup for this number.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Eligible** | **bool?** | Whether the number can run the agent; null when the terms are not accepted yet (Meta refuses the check). | 
**TermsAccepted** | **bool** | False when Meta rejects calls because the merchant has not accepted the terms in WhatsApp Manager. | 
**Onboarded** | **bool** | An agent exists on the number (onboard was called). | 
**Enabled** | **bool** | The agent answers live conversations. | 
**AgentId** | **string** |  | 
**Settings** | [**BusinessAgentSettings**](BusinessAgentSettings.md) |  | 
**ManualSteps** | [**List&lt;BusinessAgentStatusManualStepsInner&gt;**](BusinessAgentStatusManualStepsInner.md) | Steps Meta keeps outside the API that Zernio can verify are still pending. | 
**UnverifiedSteps** | [**List&lt;BusinessAgentStatusUnverifiedStepsInner&gt;**](BusinessAgentStatusUnverifiedStepsInner.md) | Steps Meta keeps outside the API and exposes no state for, listed once an agent exists. Informational: Zernio cannot tell whether the merchant already did them. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

