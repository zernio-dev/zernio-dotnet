# Zernio.Model.GetLeadForm200ResponseForm

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Status** | **string** | One of ACTIVE, ARCHIVED, DELETED or DRAFT. | [optional] 
**Locale** | **string** |  | [optional] 
**CreatedTime** | **DateTime** |  | [optional] 
**PageId** | **string** | Owning Facebook Page. A form on any other Page is a 404, whether read or archived. | [optional] 
**LeadsCount** | **int** |  | [optional] 
**OrganicLeadsCount** | **int** |  | [optional] 
**ExpiredLeadsCount** | **int** | Leads Meta has aged out of the retention window. | [optional] 
**PrivacyPolicyUrl** | **string** |  | [optional] 
**FollowUpActionUrl** | **string** |  | [optional] 
**FollowUpActionText** | **string** |  | [optional] 
**QuestionPageCustomHeadline** | **string** |  | [optional] 
**IsOptimizedForQuality** | **bool** |  | [optional] 
**BlockDisplayForNonTargetedViewer** | **bool** |  | [optional] 
**AllowOrganicLead** | **bool** | Whether the form can also be submitted from an organic Page post. | [optional] 
**TrackingParameters** | [**List&lt;BoostPostRequestTrackingUrlTagsInner&gt;**](BoostPostRequestTrackingUrlTagsInner.md) | Custom key/value pairs attached to every lead of this form. | [optional] 
**LegalContent** | [**MetaLeadFormLegalContent**](MetaLeadFormLegalContent.md) |  | [optional] 
**ContextCard** | [**MetaLeadFormContextCard**](MetaLeadFormContextCard.md) |  | [optional] 
**ThankYouPage** | [**MetaLeadFormThankYouPage**](MetaLeadFormThankYouPage.md) |  | [optional] 
**Questions** | [**List&lt;MetaLeadFormQuestionsInner&gt;**](MetaLeadFormQuestionsInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

