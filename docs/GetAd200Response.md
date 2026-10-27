# Zernio.Model.GetAd200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Ad** | [**Ad**](Ad.md) |  | [optional] 
**CachedAt** | **DateTime?** | Google RSA details cache timestamp. | [optional] 
**Stale** | **bool** | Whether Google RSA details use the last successful cached response. | [optional] 
**StatusReadAt** | **DateTime?** | With &#x60;live&#x3D;true&#x60;, when the switches were read from the platform; null when the live read failed and the stored values were returned. Always set on an unsynced Meta ad read with &#x60;accountId&#x60;, the time of that read. | [optional] 
**DarkPost** | [**GetAd200ResponseDarkPost**](GetAd200ResponseDarkPost.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

