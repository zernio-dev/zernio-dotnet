# Zernio.Model.CreateRcsAgentRequest
Send exactly one of brandId or brand.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** |  | 
**BrandId** | **string** |  | [optional] 
**Brand** | [**RcsBrandInput**](RcsBrandInput.md) |  | [optional] 
**DisplayName** | **string** | Shown as the sender name. | 
**UseCase** | **string** |  | 
**Profile** | [**RcsAgentProfile**](RcsAgentProfile.md) |  | 
**SmsFallbackFrom** | **string** | One of your SMS-enabled numbers. Phones without RCS get the message as SMS from it. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

