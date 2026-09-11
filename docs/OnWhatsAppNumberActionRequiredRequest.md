# Zernio.Model.OnWhatsAppNumberActionRequiredRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Event** | **string** |  | [optional] 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | [optional] 
**Reason** | **string** |  | [optional] 
**Requirements** | [**List&lt;OnWhatsAppNumberActionRequiredRequestRequirementsInner&gt;**](OnWhatsAppNumberActionRequiredRequestRequirementsInner.md) | Every requirement on the order with the reviewer&#39;s current verdict. Omitted when the order&#39;s requirements could not be read. | [optional] 
**ReviewedAt** | **DateTime** | When the reviewer last commented on the order. Omitted when there is no reviewer comment. | [optional] 
**Number** | [**OnWhatsAppNumberDeclinedRequestNumber**](OnWhatsAppNumberDeclinedRequestNumber.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

