# Zernio.Model.CommerceCatalogSync
A store kept in sync with an ad-platform product catalog.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**AccountId** | **string** | The store SocialAccount id. | [optional] 
**CatalogPlatform** | **string** |  | [optional] 
**CatalogAccountId** | **string** | The Meta login account whose token writes to the catalog. | [optional] 
**CatalogId** | **string** |  | [optional] 
**RunStatus** | **string** |  | [optional] 
**LastRunStartedAt** | **DateTime?** |  | [optional] 
**LastRunFinishedAt** | **DateTime?** |  | [optional] 
**LastError** | **string** | Why the last run failed, or how many items Meta rejected in a run that otherwise succeeded. Null after a clean run. | [optional] 
**ItemsSent** | **int** | Catalog items (one per variant) Meta accepted in the last full run. | [optional] 
**ItemsSkipped** | **int** | Products the last full run could not list: not published to the online store or without an image. | [optional] 
**ItemsDeleted** | **int** | Items the last full run removed because the store no longer has them. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

