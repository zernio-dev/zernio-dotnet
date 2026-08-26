# Zernio.Model.MetaLeadFormPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Questions** | [**List&lt;CreateLeadFormRequestQuestionsInner&gt;**](CreateLeadFormRequestQuestionsInner.md) |  | 
**PrivacyPolicyLinkText** | **string** |  | [optional] 
**FollowUpActionUrl** | **string** |  | [optional] 
**Locale** | **string** |  | [optional] 
**ThankYouTitle** | **string** |  | [optional] 
**ThankYouBody** | **string** |  | [optional] 
**ThankYouButtonText** | **string** |  | [optional] 
**ThankYouButtonType** | **string** |  | [optional] 
**ThankYouWebsiteUrl** | **string** |  | [optional] 
**ThankYouEnableMessenger** | **bool** | Adds a &#39;Continue in Messenger&#39; option to the thank-you page (Meta thank_you_page.enable_messenger), so the lead can carry on chatting with the Page. Set thankYouButtonType to MESSAGE_BUSINESS or P2B_MESSENGER to make the chat the primary button. | [optional] [default to false]
**IsOptimizedForQuality** | **bool** | Set true for a higher-intent form (adds a review step before submit). | [optional] 
**IsPhoneSmsVerifyEnabled** | **bool** | Requires the lead to verify their phone number over SMS before the form submits (Meta is_phone_sms_verify_enabled). Only meaningful on a form with a PHONE question. Meta can restrict this parameter to apps holding a capability: when it does, the create fails with a 422 naming platformSpecificData.isPhoneSmsVerifyEnabled, and the toggle then has to be set in Meta&#39;s form builder. | [optional] [default to false]
**BlockDisplayForNonTargetedViewer** | **bool** |  | [optional] 
**QuestionPageCustomHeadline** | **string** |  | [optional] 
**ContextCard** | [**MetaLeadFormPlatformDataContextCard**](MetaLeadFormPlatformDataContextCard.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

