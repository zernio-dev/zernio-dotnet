# Zernio.Model.CreateSipTrunkRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Label** | **string** | Display name for the trunk. | 
**SipHost** | **string** | Fully-qualified hostname inbound calls are delivered to (e.g. sip.rtc.elevenlabs.io, sip.retellai.com). | 
**SipPort** | **int** | Defaults to 5061 for tls, 5060 otherwise. | [optional] 
**Transport** | **string** | Signaling transport toward sipHost. Default tls (with SRTP media). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

