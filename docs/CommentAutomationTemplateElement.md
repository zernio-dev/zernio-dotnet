# Zernio.Model.CommentAutomationTemplateElement

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Title** | **string** | Card headline (80 chars max). Also used as the Inbox preview for the sent DM. | 
**Subtitle** | **string** | Card description, e.g. the price or a short pitch (80 chars max). | [optional] 
**ImageUrl** | **string** | Publicly reachable http(s) image rendered large above the card. | [optional] 
**Buttons** | [**List&lt;CommentAutomationTemplateElementButtonsInner&gt;**](CommentAutomationTemplateElementButtonsInner.md) | Up to 3 card buttons. A generic template has NO phone button, on either platform. &#x60;url&#x60; buttons are click-tracked when linkTracking is on. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

