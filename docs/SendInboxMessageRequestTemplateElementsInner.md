# Zernio.Model.SendInboxMessageRequestTemplateElementsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Title** | **string** | Element title (max 80 chars). Required for Instagram/Facebook generic templates. | [optional] 
**Subtitle** | **string** | Element subtitle (Instagram/Facebook only) | [optional] 
**ImageUrl** | **string** | Element image URL (Instagram/Facebook only) | [optional] 
**Buttons** | [**List&lt;SendInboxMessageRequestTemplateElementsInnerButtonsInner&gt;**](SendInboxMessageRequestTemplateElementsInnerButtonsInner.md) | Element buttons (Instagram/Facebook only) | [optional] 
**Name** | **string** | WhatsApp only. Name of the approved template to send. | [optional] 
**Language** | **string** | WhatsApp only. Template language code (e.g. en_US). | [optional] 
**Components** | **List&lt;Dictionary&lt;string, Object&gt;&gt;** | WhatsApp only. Meta Cloud API send-shape components array, forwarded to Meta verbatim. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

