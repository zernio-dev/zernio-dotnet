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
**ThankYouButtonType** | **string** | Meta thank_you_page.button_type. Defaults to VIEW_WEBSITE. Case-insensitive, sent to Meta in uppercase. CALL_BUSINESS requires businessPhoneNumber and countryCode (a 400 otherwise). Meta rejects MESSAGE_BUSINESS on thank-you pages with (#100) This button type is not yet supported for Thank You Page. | [optional] 
**BusinessPhoneNumber** | **string** | International E.164 number the CALL_BUSINESS thank-you button dials (Meta thank_you_page.business_phone_number). It must start with + and the country calling code matching countryCode; spaces, dashes, dots and parentheses are stripped, and a local number such as 2025550123 is a 400. Required when thankYouButtonType is CALL_BUSINESS and a 400 with any other button type. Accepted only inside platformSpecificData: a top-level businessPhoneNumber is a 400. | [optional] 
**CountryCode** | **string** | ISO 3166-1 alpha-2 country of businessPhoneNumber (Meta thank_you_page.country_code), sent in uppercase. Required when thankYouButtonType is CALL_BUSINESS and a 400 with any other button type. Accepted only inside platformSpecificData: a top-level countryCode is a 400. | [optional] 
**ThankYouWebsiteUrl** | **string** |  | [optional] 
**ThankYouEnableMessenger** | **bool** | Sent as Meta thank_you_page.enable_messenger (boolean). Accepted only inside platformSpecificData: a top-level thankYouEnableMessenger is a 400. | [optional] [default to false]
**IsOptimizedForQuality** | **bool** | Set true for a higher-intent form (adds a review step before submit). | [optional] 
**IsPhoneSmsVerifyEnabled** | **bool** | Requires the lead to verify their phone number over SMS before the form submits (Meta is_phone_sms_verify_enabled). Only meaningful on a form with a PHONE question. Meta can restrict this parameter to apps holding a capability: when it does, the create fails with a 422 naming platformSpecificData.isPhoneSmsVerifyEnabled, and the toggle then has to be set in Meta&#39;s form builder. | [optional] [default to false]
**BlockDisplayForNonTargetedViewer** | **bool** |  | [optional] 
**QuestionPageCustomHeadline** | **string** |  | [optional] 
**ContextCard** | [**MetaLeadFormPlatformDataContextCard**](MetaLeadFormPlatformDataContextCard.md) |  | [optional] 
**CustomDisclaimer** | [**MetaLeadFormPlatformDataCustomDisclaimer**](MetaLeadFormPlatformDataCustomDisclaimer.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

