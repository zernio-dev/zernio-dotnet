# Zernio.Model.EmailSignature
A signature Zernio stores and appends itself, so it works on every provider.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Html** | **string** |  | [optional] 
**Text** | **string** | Appended to plain-text bodies. When &#x60;null&#x60;, the html stripped to text is used. | [optional] 
**AccountId** | **string** | &#x60;null&#x60; for a workspace-wide signature. | [optional] 
**DefaultFor** | **List&lt;string&gt;** | Sending addresses this signature is the default for. Each address has one default per scope; an account signature wins over a workspace one. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**UpdatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

