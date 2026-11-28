# Zernio.Model.MetaSavedAudience
A Meta saved audience (Meta's SavedAudience node), read live from Meta.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Meta saved audience id. | [optional] 
**Name** | **string** |  | [optional] 
**Description** | **string** |  | [optional] 
**ApproximateCountLowerBound** | **int?** | Meta&#39;s estimated lower bound on reach. | [optional] 
**ApproximateCountUpperBound** | **int?** | Meta&#39;s estimated upper bound on reach. | [optional] 
**RunStatus** | **string** | Meta&#39;s run_status: whether the saved audience is active or deleted. | [optional] 
**SentenceLines** | **List&lt;Object&gt;** | Meta&#39;s human-readable targeting summary lines, passed through as Meta returns them. | [optional] 
**Targeting** | **Dictionary&lt;string, Object&gt;** | The Meta targeting spec saved in the audience, in Meta&#39;s own snake_case shape. Send it as &#x60;rawTargeting&#x60; on &#x60;POST /v1/ads/create&#x60; to target an ad set at this audience. | [optional] 
**CreatedAt** | **string** | Meta&#39;s time_created. | [optional] 
**UpdatedAt** | **string** | Meta&#39;s time_updated. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

