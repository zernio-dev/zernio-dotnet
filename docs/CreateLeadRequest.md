# Zernio.Model.CreateLeadRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** | The profile the lead belongs to. | 
**Email** | **string** | Required unless phone is given. | [optional] 
**Phone** | **string** | Required unless email is given. E.164 is best. | [optional] 
**Fields** | **Dictionary&lt;string, string&gt;** | Other answers, field name to value (&#x60;full_name&#x60;, &#x60;company&#x60;, ...). Stored on the lead, never sent to an ad platform. | [optional] 
**FormId** | **string** | Your id for the form. Defaults to &#x60;api&#x60;. | [optional] 
**FormName** | **string** |  | [optional] 
**LeadId** | **string** | Your id for this lead (a CRM id, a submission id). Makes the call idempotent. | [optional] 
**SubmittedAt** | **DateTime** | When the form was submitted. Defaults to now. | [optional] 
**SourceUrl** | **string** | The page the form was submitted on, with its query string. | [optional] 
**VisitorId** | **string** | The Zernio tag visitor id, from the &#x60;_zid&#x60; cookie. | [optional] 
**ClickIds** | **Dictionary&lt;string, string&gt;** | Ad click and browser ids: &#x60;fbclid&#x60; or &#x60;fbc&#x60;, &#x60;fbp&#x60;, &#x60;gclid&#x60;, &#x60;gbraid&#x60;, &#x60;wbraid&#x60;, &#x60;ttclid&#x60;, &#x60;msclkid&#x60;, &#x60;li_fat_id&#x60;, ... | [optional] 
**Utm** | **Dictionary&lt;string, string&gt;** | &#x60;utm_source&#x60;, &#x60;utm_campaign&#x60;, ... | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

