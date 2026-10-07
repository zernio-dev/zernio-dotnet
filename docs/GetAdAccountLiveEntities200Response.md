# Zernio.Model.GetAdAccountLiveEntities200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | [optional] 
**AdAccountId** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**Currency** | **string** | ISO 4217 code every budget and bid amount is expressed in. | [optional] 
**ReadAt** | **DateTime** | When the platform was read. | [optional] 
**Campaigns** | [**List&lt;GetAdAccountLiveEntities200ResponseCampaignsInner&gt;**](GetAdAccountLiveEntities200ResponseCampaignsInner.md) | Absent when &#x60;level&#x3D;adSet&#x60;. | [optional] 
**AdSets** | [**List&lt;GetAdAccountLiveEntities200ResponseAdSetsInner&gt;**](GetAdAccountLiveEntities200ResponseAdSetsInner.md) | Absent when &#x60;level&#x3D;campaign&#x60;. | [optional] 
**Paging** | [**GetAdAccountLiveEntities200ResponsePaging**](GetAdAccountLiveEntities200ResponsePaging.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

