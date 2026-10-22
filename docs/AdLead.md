# Zernio.Model.AdLead

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Zernio lead id. | [optional] 
**LeadgenId** | **string** | Meta lead id. On LinkedIn, the leadFormResponse id. | [optional] 
**FormId** | **string** |  | [optional] 
**FormName** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**AdId** | **string** |  | [optional] 
**AdsetId** | **string** |  | [optional] 
**CampaignId** | **string** | On LinkedIn, this is the LinkedIn Campaign id, which corresponds to platformAdSetId on GET /v1/ads (LinkedIn&#39;s Campaign Group is Zernio&#39;s campaign). | [optional] 
**IsOrganic** | **bool** |  | [optional] 
**CreatedTime** | **string** | ISO 8601. | [optional] 
**Fields** | **Dictionary&lt;string, string&gt;** | Question key → answer. On LinkedIn, the key is the lowercased predefinedField, else the question name, else the numeric questionId; multiple-choice values are option labels (unlike Meta, which returns the option key). | [optional] 
**FieldData** | **List&lt;Object&gt;** | Raw Meta field_data. | [optional] 
**Status** | **string** | Meta leads only. &#x60;contacted&#x60; is set when the first WhatsApp message of a lead_received workflow is delivered, &#x60;unreachable&#x60; when it fails or the phone number is not valid. | [optional] 
**StatusChangedAt** | **DateTime?** |  | [optional] 
**Value** | **decimal?** |  | [optional] 
**Currency** | **string** |  | [optional] 
**ContactId** | **string** | The contact a lead_received workflow created or matched for this lead. | [optional] 
**FirstContactedAt** | **DateTime?** | When the first WhatsApp message to the lead was delivered. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

