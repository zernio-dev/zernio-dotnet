# Zernio.Model.RequestPhoneNumberWhatsAppCode200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Message** | **string** |  | [optional] 
**Method** | **string** |  | [optional] 
**AlreadyVerified** | **bool** | Meta already reports the number as verified. No code is sent and the number is activated. | [optional] 
**Replaced** | **bool** | Meta refused the original number, which had never been live, so it was replaced on the same record. | [optional] 
**NewPhoneNumber** | **string** | The replacement number, present when &#x60;replaced&#x60; is true. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

