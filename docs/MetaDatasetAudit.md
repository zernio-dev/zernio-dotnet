# Zernio.Model.MetaDatasetAudit

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | 
**AdAccountId** | **string** |  | 
**Dataset** | [**MetaDatasetAuditDataset**](MetaDatasetAuditDataset.md) |  | 
**Datasets** | [**List&lt;MetaDatasetAuditDatasetsInner&gt;**](MetaDatasetAuditDatasetsInner.md) | Every pixel assigned to the ad account. | 
**Window** | [**MetaDatasetAuditWindow**](MetaDatasetAuditWindow.md) |  | 
**Events** | [**List&lt;MetaDatasetAuditEventsInner&gt;**](MetaDatasetAuditEventsInner.md) | One entry per event Meta counted in the window or scored, busiest first. | 
**Findings** | [**List&lt;MetaDatasetAuditFindingsInner&gt;**](MetaDatasetAuditFindingsInner.md) | Problems the numbers show, most damaging first. | 
**Unavailable** | [**List&lt;MetaDatasetAuditUnavailableInner&gt;**](MetaDatasetAuditUnavailableInner.md) | What the audit could not read, and why. | 
**CheckedAt** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

