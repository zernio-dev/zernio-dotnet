# Zernio.Model.GetAdAccountHierarchy200ResponseRootsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **string** | Native Google Ads customer id, digits only. | [optional] 
**Name** | **string** |  | [optional] 
**Currency** | **string** | ISO 4217 code. | [optional] 
**VarTimeZone** | **string** | IANA time zone, e.g. Europe/Madrid. | [optional] 
**Manager** | **bool** | True for a manager (MCC) account. | [optional] 
**TestAccount** | **bool** |  | [optional] 
**Status** | **string** | Google customer status: ENABLED, CANCELED, SUSPENDED or CLOSED. | [optional] 
**ManagerLinks** | [**List&lt;GetAdAccountHierarchy200ResponseRootsInnerManagerLinksInner&gt;**](GetAdAccountHierarchy200ResponseRootsInnerManagerLinksInner.md) | Managers linked to this account, ACTIVE or PENDING. | [optional] 
**Clients** | [**List&lt;GoogleAdsHierarchyClient&gt;**](GoogleAdsHierarchyClient.md) | Every account under this root at any depth, in Google&#39;s order, followed by pending invitations. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

