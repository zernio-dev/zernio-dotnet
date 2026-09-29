# Zernio.Model.ImessageSandboxContact

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Handle** | **string** | Phone (E.164) or lowercase Apple ID email | [optional] 
**Status** | **string** |  | [optional] 
**JoinText** | **string** | Send this from the handle to the sandbox line to activate it | [optional] 
**JoinLink** | **string** | Opens Messages on the sandbox line with joinText prefilled | [optional] 
**ActivatedAt** | **DateTime?** |  | [optional] 
**LastInboundAt** | **DateTime?** | Replies are allowed for 24 hours after this | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

