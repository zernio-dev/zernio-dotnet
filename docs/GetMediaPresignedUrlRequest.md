# Zernio.Model.GetMediaPresignedUrlRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Filename** | **string** | Name of the file to upload | 
**ContentType** | **string** | MIME type of the file | 
**Size** | **int** | Optional file size in bytes for pre-validation (max 5GB) | [optional] 
**Permanent** | **bool** | Write the file to permanent storage instead of temporary storage. Temporary files auto-delete 7 days after upload; permanent files never expire. | [optional] [default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

