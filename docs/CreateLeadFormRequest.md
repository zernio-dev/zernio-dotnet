# Zernio.Model.CreateLeadFormRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | 
**Name** | **string** |  | 
**Questions** | [**List&lt;CreateLeadFormRequestQuestionsInner&gt;**](CreateLeadFormRequestQuestionsInner.md) |  | 
**PrivacyPolicyUrl** | **string** |  | 
**PrivacyPolicyLinkText** | **string** |  | [optional] 
**FollowUpActionUrl** | **string** |  | [optional] 
**Locale** | **string** |  | [optional] 
**ThankYouTitle** | **string** |  | [optional] 
**ThankYouBody** | **string** |  | [optional] 
**ThankYouButtonText** | **string** |  | [optional] 
**ThankYouButtonType** | **string** |  | [optional] 
**ThankYouWebsiteUrl** | **string** |  | [optional] 
**IsOptimizedForQuality** | **bool** | Legacy form type toggle. Prefer formType instead. false &#x3D; More Volume, true &#x3D; Higher Intent. | [optional] 
**FormType** | **string** | Form type. MORE_VOLUME &#x3D; optimized for lead quantity (default). HIGHER_INTENT &#x3D; adds a review/confirmation step before submit. RICH_CREATIVE &#x3D; includes context card and custom headline to educate users before they submit. Supersedes isOptimizedForQuality. | [optional] 
**BlockDisplayForNonTargetedViewer** | **bool** | Sharing setting. true &#x3D; Restricted (only people targeted by the ad can open the form link). false &#x3D; Open (shareable link, default). | [optional] 
**AllowOrganicLeadGen** | **bool** | Flexible form delivery. true &#x3D; the form can surface organically on the Page (not just as a paid ad). Defaults to false. | [optional] 
**QuestionPageCustomHeadline** | **string** | Custom subheadline shown above the form fields on the questions page (the contact-information section description). Defaults to Meta&#39;s generic copy when omitted. | [optional] 
**ContextCard** | [**CreateLeadFormRequestContextCard**](CreateLeadFormRequestContextCard.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

