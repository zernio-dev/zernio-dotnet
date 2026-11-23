# Zernio.Model.TransferVoiceCallRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**To** | **string** | +E164 phone number (tel: prefix optional) or a sip: URI. wss:// is not a valid transfer target. | 
**CallerId** | **string** | Caller ID shown on the transfer leg. &#x60;business&#x60; is your own number. &#x60;caller&#x60; is the original caller&#39;s number, for inbound calls only. The carrier may refuse &#x60;caller&#x60; on some routes: you get a 422, then retry with &#x60;business&#x60;. | [optional] [default to CallerIdEnum.Business]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

