# Zernio.Model.EmailLabel
A Gmail label or an Outlook category. Outlook categories are addressed by name, so their `id` is the name.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Gmail label id such as &#x60;Label_12&#x60;, or the Outlook category name. | [optional] 
**AccountId** | **string** |  | [optional] 
**Provider** | **string** |  | [optional] 
**Name** | **string** | Gmail nests labels with a slash, as in &#x60;Hermia/Handled&#x60;. | [optional] 
**Type** | **string** |  | [optional] 
**Color** | [**EmailLabelColor**](EmailLabelColor.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

