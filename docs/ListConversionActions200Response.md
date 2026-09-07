# Zernio.Model.ListConversionActions200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **string** | The Google Ads customer id the actions were read from. | [optional] 
**Actions** | [**List&lt;ConversionAction&gt;**](ConversionAction.md) |  | [optional] 
**CachedAt** | **DateTime?** | When this list was fetched from Google. Null when it was never served from cache. | [optional] 
**Stale** | **bool** | True when Google&#39;s daily API quota was exhausted and this is the last successful fetch, not a live read. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

