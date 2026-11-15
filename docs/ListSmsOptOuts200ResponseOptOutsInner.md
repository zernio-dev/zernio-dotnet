# Zernio.Model.ListSmsOptOuts200ResponseOptOutsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PhoneNumber** | **string** |  | [optional] 
**OptedOutAt** | **DateTime?** |  | [optional] 
**Keyword** | **string** | The keyword they sent (e.g. STOP), when the carrier recorded one. | [optional] 
**From** | **string** | Which of your numbers the recipient opted out from. | [optional] 
**Source** | **string** | &#x60;inbound_stop&#x60; when the recipient texted an opt-out keyword, &#x60;api&#x60; when recorded with &#x60;POST /v1/sms/opt-outs&#x60;. Null when unknown. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

