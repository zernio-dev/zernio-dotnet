# Zernio.Model.Lead
A single lead submission returned by the leads endpoint and the lead.received webhook.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Meta &#x60;leadgen_id&#x60;. | [optional] 
**CreatedTime** | **DateTime** |  | [optional] 
**AdId** | **string** | Meta ad ID that surfaced the form. Organic leads omit this. | [optional] 
**FormId** | **string** |  | [optional] 
**Fields** | **Dictionary&lt;string, string&gt;** | Flattened key→value map of answers (multi-value fields joined with \&quot;, \&quot;). | [optional] 
**FieldData** | [**List&lt;LeadFieldDataInner&gt;**](LeadFieldDataInner.md) | Raw &#x60;field_data&#x60; from Meta (one entry per question). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

