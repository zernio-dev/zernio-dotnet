# Zernio.Model.GetAdAccountHierarchy200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | [optional] 
**Roots** | [**List&lt;GetAdAccountHierarchy200ResponseRootsInner&gt;**](GetAdAccountHierarchy200ResponseRootsInner.md) |  | [optional] 
**DirectCustomers** | [**List&lt;GetAdAccountHierarchy200ResponseDirectCustomersInner&gt;**](GetAdAccountHierarchy200ResponseDirectCustomersInner.md) |  | [optional] 
**Unavailable** | [**List&lt;GetAdAccountHierarchy200ResponseUnavailableInner&gt;**](GetAdAccountHierarchy200ResponseUnavailableInner.md) |  | [optional] 
**Truncated** | **bool** |  | [optional] 
**CachedAt** | **DateTime?** | When this data was fetched from Google. Null on a live read. | [optional] 
**Stale** | **bool** | True when Google&#39;s quota was exhausted and this is the last successful fetch. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

