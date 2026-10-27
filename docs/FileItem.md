# Zernio.Model.FileItem
A file or folder in a connected Google Drive or OneDrive. Ids are the provider's own.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**AccountId** | **string** |  | 
**Provider** | **string** |  | 
**Name** | **string** |  | 
**Kind** | **string** |  | 
**MimeType** | **string** |  | 
**Size** | **int?** | Bytes; null for folders and Google editors files. | 
**ParentId** | **string** |  | 
**WebUrl** | **string** | The provider&#39;s own link to open the item. | 
**Downloadable** | **bool** | False for folders and for Drive files whose owner disabled downloading. | 
**ExportMimeType** | **string** | Google Docs, Slides and Drawings download as PDF/PNG and Sheets as XLSX; this is the type the download carries. | [optional] 
**CreatedAt** | **DateTime?** |  | 
**ModifiedAt** | **DateTime?** |  | 
**Trashed** | **bool** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

