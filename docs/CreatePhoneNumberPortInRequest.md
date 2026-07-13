# Zernio.Model.CreatePhoneNumberPortInRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PhoneNumbers** | **List&lt;string&gt;** | E.164 numbers to port in. | 
**EndUser** | [**CreatePhoneNumberPortInRequestEndUser**](CreatePhoneNumberPortInRequestEndUser.md) |  | 
**LoaDocumentId** | **string** | Document id from POST /v1/phone-numbers/port-in/documents (kind&#x3D;loa). | 
**InvoiceDocumentId** | **string** | Document id from POST /v1/phone-numbers/port-in/documents (kind&#x3D;invoice). | 
**FocDatetimeRequested** | **DateTime** | Requested port date; the carrier confirms the actual FOC later. Defaults to one week out (shifted off weekends) when omitted. | [optional] 
**CustomerReference** | **string** |  | [optional] 
**PortType** | **string** | Whether the losing account ports all its numbers (full) or keeps some (partial). | [optional] [default to PortTypeEnum.Full]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

