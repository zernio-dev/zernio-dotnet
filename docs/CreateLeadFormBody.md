# Zernio.Model.CreateLeadFormBody

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Facebook social account ID (Late SocialAccount _id). | 
**Name** | **string** |  | 
**Questions** | [**List&lt;LeadGenFormQuestion&gt;**](LeadGenFormQuestion.md) |  | 
**PrivacyPolicyUrl** | **string** | Required by Meta. Must be reachable from Meta&#39;s crawler. | 
**PrivacyPolicyLinkText** | **string** |  | [optional] 
**FollowUpActionUrl** | **string** |  | [optional] 
**Locale** | **string** |  | [optional] 
**ThankYouTitle** | **string** |  | [optional] 
**ThankYouBody** | **string** |  | [optional] 
**ThankYouButtonText** | **string** |  | [optional] 
**ThankYouButtonType** | **string** | Meta enum (e.g. VIEW_WEBSITE, CALL_BUSINESS, DOWNLOAD) | [optional] 
**ThankYouWebsiteUrl** | **string** |  | [optional] 
**IsOptimizedForQuality** | **bool** |  | [optional] 
**ContextCard** | [**CreateLeadFormBodyContextCard**](CreateLeadFormBodyContextCard.md) |  | [optional] 
**LegalContent** | [**CreateLeadFormBodyLegalContent**](CreateLeadFormBodyLegalContent.md) |  | [optional] 
**TrackingParameters** | **Dictionary&lt;string, string&gt;** | Up to 20 key/value pairs surfaced on every lead for attribution. | [optional] 
**QuestionPageCustomHeadline** | **string** |  | [optional] 
**AllowOrganicLead** | **bool** |  | [optional] 
**BlockDisplayForNonTargetedViewer** | **bool** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

