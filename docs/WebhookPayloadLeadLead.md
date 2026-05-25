# Zernio.Model.WebhookPayloadLeadLead

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Zernio lead ID (AdLead document ID) | 
**LeadgenId** | **string** | Meta lead ID (the platform&#39;s leadgen_id) | 
**FormId** | **string** | Lead Gen form ID the lead was submitted against | 
**FormName** | **string** | Human-readable form name (best-effort; may be null) | [optional] 
**AdId** | **string** | Meta ad ID that drove the lead (null for organic/test leads) | [optional] 
**AdsetId** | **string** |  | [optional] 
**CampaignId** | **string** |  | [optional] 
**Fields** | **Dictionary&lt;string, string&gt;** | Flattened question key -&gt; answer map. For multiple-choice questions the value is the option key (e.g. \&quot;k1\&quot;), not the display label.  | 
**IsOrganic** | **bool** | True when the lead came from an organic post rather than a paid ad | 
**CreatedAt** | **DateTime** | Meta&#39;s lead creation time (ISO 8601) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

