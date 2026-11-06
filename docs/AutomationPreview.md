# Zernio.Model.AutomationPreview
What an ad rule would do if it ran now. Nothing is changed. Cooldowns and daily caps are left out, so a run right after can act on fewer objects. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EvaluatedAt** | **DateTime** |  | 
**Today** | **DateOnly** | Today in the ad account timezone. | 
**Timezone** | **string** |  | 
**TimezoneAssumed** | **bool** | True when the ad account timezone is unknown and UTC was used. | 
**Currency** | **string** |  | 
**Evaluated** | **int** |  | 
**Matched** | **int** |  | 
**Truncated** | **bool** | True when more subjects were judged than &#x60;limit&#x60; lists. | 
**Subjects** | [**List&lt;AutomationPreviewSubjectsInner&gt;**](AutomationPreviewSubjectsInner.md) | Matches first, up to &#x60;limit&#x60;. | 
**Groups** | [**List&lt;AutomationPreviewGroupsInner&gt;**](AutomationPreviewGroupsInner.md) | Each group&#39;s totals against the conditions, when the rule has &#x60;subjects.groups&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

