# Zernio.Model.SendEvents200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EventsReceived** | **int** | Events in the request. | [optional] 
**Stored** | **bool** | Whether the events were stored for reporting (always false with testCode). | [optional] 
**TestCode** | **string** | The test code forwarded to every destination, or &#x60;null&#x60; when the request carried none. | [optional] 
**Destinations** | [**List&lt;SendEvents200ResponseDestinationsInner&gt;**](SendEvents200ResponseDestinationsInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

