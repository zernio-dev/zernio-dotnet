# Zernio.Model.GetWhatsAppTemplate200ResponseTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Meta template id. Unique per language variant; usable on /v1/whatsapp/templates/id/{templateId}. | [optional] 
**Name** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**Category** | **string** |  | [optional] 
**Language** | **string** | The variant actually returned. | [optional] 
**Components** | **List&lt;Object&gt;** |  | [optional] 
**RejectedReason** | **string** | Only when status is REJECTED. | [optional] 
**QualityScore** | **Object** | Post-approval quality (GREEN/YELLOW/RED), when Meta reports one. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

