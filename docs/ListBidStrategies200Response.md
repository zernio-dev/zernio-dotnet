# Zernio.Model.ListBidStrategies200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **string** |  | [optional] 
**Currency** | **string** | Account currency code; money fields are in this currency&#39;s units. | [optional] 
**Strategies** | [**List&lt;PortfolioBidStrategy&gt;**](PortfolioBidStrategy.md) |  | [optional] 
**CachedAt** | **DateTime?** | When this data was fetched from Google. Null when it was never served from cache. | [optional] 
**Stale** | **bool** | True when Google&#39;s daily API quota was exhausted and this is the last successful fetch, not a live read. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

