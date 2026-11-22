# Zernio.Model.AutomationOneOf3

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Description** | **string** |  | [optional] 
**Status** | **string** | Only a sequence or a flow can be a draft. | 
**Trigger** | [**SequenceAutomationDefinitionTrigger**](SequenceAutomationDefinitionTrigger.md) |  | 
**Steps** | [**List&lt;AutomationSequenceStep&gt;**](AutomationSequenceStep.md) | At least one step for an active sequence. Steps change only while it is a draft or paused. | 
**Limits** | [**SequenceAutomationDefinitionLimits**](SequenceAutomationDefinitionLimits.md) |  | [optional] 
**Id** | **string** |  | 
**Kind** | **string** |  | 
**VarVersion** | **string** | Send it back as &#x60;If-Match&#x60; when editing, so an edit made after someone else saved is refused. | 
**LastCheckAt** | **DateTime** | Null until an ad rule first checks. Always null for every other kind; the checks of event and scheduled automations list when they ran. | 
**NextCheckAt** | **DateTime** | Null while paused. Always null for every kind but ad rules. | 
**CreatedAt** | **DateTime** |  | 
**UpdatedAt** | **DateTime** |  | 
**Template** | [**AutomationRecordTemplate**](AutomationRecordTemplate.md) |  | [optional] 
**Platform** | **string** | The account&#39;s platform. On &#x60;whatsapp&#x60; every step sends a template. | 
**Enrollments** | [**AutomationOneOf3AllOfEnrollments**](AutomationOneOf3AllOfEnrollments.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

