# Zernio.Model.ListWhatsAppConversions200ResponseEventsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Timestamp** | **DateTime** | When the event was sent to Meta. | [optional] 
**EventName** | **string** | One of LeadSubmitted, Purchase, AddToCart, InitiateCheckout, ViewContent. | [optional] 
**ConversationId** | **string** |  | [optional] 
**EventsReceived** | **int** | Number of events Meta accepted on this send (usually 1). | [optional] 
**EventsFailed** | **int** | Number of events Meta rejected (usually 0). | [optional] 
**TraceId** | **string** | Meta fbtrace_id for cross-referencing in Events Manager. | [optional] 
**DurationMs** | **int** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

