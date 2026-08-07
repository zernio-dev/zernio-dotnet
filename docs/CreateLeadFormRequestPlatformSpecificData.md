# Zernio.Model.CreateLeadFormRequestPlatformSpecificData
Form content; the shape is selected by the accountId's platform. Unknown fields are a 400 (strict-parsed).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Questions** | [**List&lt;LinkedInLeadFormPlatformDataQuestionsInner&gt;**](LinkedInLeadFormPlatformDataQuestionsInner.md) |  | 
**PrivacyPolicyLinkText** | **string** |  | [optional] 
**FollowUpActionUrl** | **string** |  | [optional] 
**Locale** | [**LinkedInLeadFormPlatformDataLocale**](LinkedInLeadFormPlatformDataLocale.md) |  | [optional] 
**ThankYouTitle** | **string** |  | [optional] 
**ThankYouBody** | **string** |  | [optional] 
**ThankYouButtonText** | **string** |  | [optional] 
**ThankYouButtonType** | **string** |  | [optional] 
**ThankYouWebsiteUrl** | **string** |  | [optional] 
**IsOptimizedForQuality** | **bool** | Set true for a higher-intent form (adds a review step before submit). | [optional] 
**BlockDisplayForNonTargetedViewer** | **bool** |  | [optional] 
**QuestionPageCustomHeadline** | **string** |  | [optional] 
**ContextCard** | [**MetaLeadFormPlatformDataContextCard**](MetaLeadFormPlatformDataContextCard.md) |  | [optional] 
**AdAccountId** | **string** | LinkedIn ad account id (resolves the owning organization). | 
**Headline** | **string** |  | 
**Description** | **string** |  | 
**State** | **string** | Defaults to DRAFT. | [optional] 
**Consents** | [**List&lt;LinkedInLeadFormPlatformDataConsentsInner&gt;**](LinkedInLeadFormPlatformDataConsentsInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

