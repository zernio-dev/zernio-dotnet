# Zernio.Model.GoogleAdsHierarchyClient
A Google Ads account inside a manager tree.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **string** | Native Google Ads customer id, digits only. | [optional] 
**Name** | **string** | Null for a pending invitation. | [optional] 
**Currency** | **string** |  | [optional] 
**VarTimeZone** | **string** |  | [optional] 
**Manager** | **bool** | True for a sub-manager account. | [optional] 
**TestAccount** | **bool** |  | [optional] 
**Hidden** | **bool** | Hidden in the manager&#39;s Google Ads UI. | [optional] 
**Level** | **int** | Distance from the root (1 &#x3D; direct client of the root). | [optional] 
**Status** | **string** | Google customer status: ENABLED, CANCELED, SUSPENDED or CLOSED. Null for a pending invitation. | [optional] 
**ParentCustomerId** | **string** | Direct manager of this account. Null only when more than 50 managers under the root were skipped. | [optional] 
**ManagerLinkId** | **string** | Id of the link to the parent, used by PATCH /v1/ads/accounts/manager-links. | [optional] 
**LinkStatus** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

