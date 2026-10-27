# Zernio.Model.ListFormLeads200ResponseLeadsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Meta leadgenId. | [optional] 
**LeadId** | **string** | Zernio lead id, for PATCH /v1/ads/leads/{id}. Only on persisted leads. | [optional] 
**Status** | **string** | Lead status (see PATCH /v1/ads/leads/{id}). Only on persisted leads. | [optional] 
**CreatedTime** | **string** |  | [optional] 
**AdId** | **string** |  | [optional] 
**FormId** | **string** |  | [optional] 
**Fields** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**FieldData** | **List&lt;Object&gt;** |  | [optional] 
**Consents** | [**List&lt;AdLeadConsent&gt;**](AdLeadConsent.md) | Meta lead forms only: the answer to every custom disclaimer checkbox, required or optional. Empty when the form has none, and may be empty on leads stored before 2026-10-22. LinkedIn leads do not carry the field. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

