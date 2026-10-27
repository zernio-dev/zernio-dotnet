# Zernio.Model.GetAdMedia200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdId** | **string** |  | [optional] 
**Platform** | **string** | &#39;facebook&#39; or &#39;instagram&#39;. Only Meta is supported for now. | [optional] 
**Synced** | **bool** | False when the ad was read live from Meta because it is not in Zernio&#39;s store (request made with &#x60;accountId&#x60;). | [optional] 
**Media** | [**List&lt;GetAdMedia200ResponseMediaInner&gt;**](GetAdMedia200ResponseMediaInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

