# Zernio.Model.GetLeadForm200ResponseForm
Full form config — sufficient to duplicate the form via POST /v1/ads/lead-forms.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Status** | **string** | ARCHIVED forms can&#39;t receive new leads. | [optional] 
**Locale** | **string** |  | [optional] 
**CreatedTime** | **DateTime** |  | [optional] 
**LeadsCount** | **int** |  | [optional] 
**PrivacyPolicyUrl** | **string** |  | [optional] 
**FollowUpActionUrl** | **string** |  | [optional] 
**Questions** | [**List&lt;GetLeadForm200ResponseFormQuestionsInner&gt;**](GetLeadForm200ResponseFormQuestionsInner.md) |  | [optional] 
**ThankYouPage** | [**GetLeadForm200ResponseFormThankYouPage**](GetLeadForm200ResponseFormThankYouPage.md) |  | [optional] 
**ContextCard** | **Object** | Intro card shown before the form questions (title, content, button label). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

