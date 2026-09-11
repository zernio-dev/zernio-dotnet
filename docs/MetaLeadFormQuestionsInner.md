# Zernio.Model.MetaLeadFormQuestionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Key** | **string** |  | [optional] 
**Label** | **string** |  | [optional] 
**Type** | **string** | EMAIL, PHONE, FULL_NAME, CUSTOM, ... | [optional] 
**InlineContext** | **string** |  | [optional] 
**Options** | [**List&lt;BoostPostRequestTrackingUrlTagsInner&gt;**](BoostPostRequestTrackingUrlTagsInner.md) |  | [optional] 
**ConditionalQuestionsGroupId** | **string** | READ-ONLY. Conditional logic can only be authored in Meta form builder; Meta has no create parameter for it. | [optional] 
**ConditionalQuestionsChoices** | **List&lt;Object&gt;** | READ-ONLY. Which answers reveal the conditional group. | [optional] 
**DependentConditionalQuestions** | **List&lt;Object&gt;** | READ-ONLY. Questions revealed by the conditional group. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

