# Zernio.Model.GetAutomationCatalog200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Schema** | **Object** | JSON Schema of the body of &#x60;POST /v1/automations&#x60;. | 
**Triggers** | [**List&lt;GetAutomationCatalog200ResponseTriggersInner&gt;**](GetAutomationCatalog200ResponseTriggersInner.md) |  | 
**Subjects** | [**List&lt;GetAutomationCatalog200ResponseSubjectsInner&gt;**](GetAutomationCatalog200ResponseSubjectsInner.md) | Ad rule subjects. | 
**Filters** | **Object** | The fields and operators &#x60;subjects.filters&#x60; takes, and which fields each subject accepts. | 
**Groups** | **Object** | What &#x60;subjects.groups&#x60; takes. | 
**Alert** | **Object** | The most checks &#x60;alert.confirmChecks&#x60; can ask for. | 
**Conditions** | **Object** | Condition operators, windows, &#x60;compareTo&#x60; options and size limits. | 
**Limits** | **List&lt;string&gt;** |  | 
**Approval** | **Object** | Where &#x60;approval.request&#x60; goes, how many approvers and how long it can wait. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

