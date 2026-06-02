# Zernio.Model.GetWhatsAppPhoneNumbers200ResponseSandbox
The shared WhatsApp sandbox (one Zernio-owned number, all users test against it). Present when the sandbox is configured; null otherwise. The `accountId` lets you address the sandbox in compose endpoints. `template` is the only template a sandbox send is allowed to use. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PhoneNumber** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**Template** | [**GetWhatsAppPhoneNumbers200ResponseSandboxTemplate**](GetWhatsAppPhoneNumbers200ResponseSandboxTemplate.md) |  | [optional] 
**IsSandbox** | **bool** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

