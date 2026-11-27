# Zernio.Model.CreateLeadFormRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to store this write as a staged change instead of applying it. The response is &#x60;202&#x60; with the change, and POST /v1/ads/changes/{changeId}/confirm applies it later. Cannot be combined with &#x60;validateOnly&#x60;. | [optional] 
**AccountId** | **string** |  | 
**Name** | **string** |  | 
**Questions** | [**List&lt;CreateLeadFormRequestQuestionsInner&gt;**](CreateLeadFormRequestQuestionsInner.md) | Deprecated (Meta legacy shape): use platformSpecificData.questions. | [optional] 
**PrivacyPolicyUrl** | **string** |  | 
**PrivacyPolicyLinkText** | **string** | Deprecated: use platformSpecificData.privacyPolicyLinkText. | [optional] 
**FollowUpActionUrl** | **string** | Deprecated: use platformSpecificData.followUpActionUrl. | [optional] 
**Locale** | **string** | Deprecated: use platformSpecificData.locale. | [optional] 
**ThankYouTitle** | **string** | Deprecated: use platformSpecificData.thankYouTitle. | [optional] 
**ThankYouBody** | **string** | Deprecated: use platformSpecificData.thankYouBody. | [optional] 
**ThankYouButtonText** | **string** | Deprecated: use platformSpecificData.thankYouButtonText. | [optional] 
**ThankYouButtonType** | **string** | Deprecated: use platformSpecificData.thankYouButtonType. | [optional] 
**ThankYouWebsiteUrl** | **string** | Deprecated: use platformSpecificData.thankYouWebsiteUrl. | [optional] 
**IsOptimizedForQuality** | **bool** | Deprecated: use platformSpecificData.isOptimizedForQuality. | [optional] 
**PlatformSpecificData** | [**CreateLeadFormRequestPlatformSpecificData**](CreateLeadFormRequestPlatformSpecificData.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

