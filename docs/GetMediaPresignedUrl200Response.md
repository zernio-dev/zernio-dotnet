# Zernio.Model.GetMediaPresignedUrl200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UploadUrl** | **string** | Presigned URL to PUT your file to (expires in 1 hour) | [optional] 
**PublicUrl** | **string** | Public URL where the file will be accessible after upload. Served from the temp/ prefix by default (expires 7 days after upload) or from media/ when permanent is true. | [optional] 
**Key** | **string** | Storage key/path of the file. Prefixed temp/ by default, media/ when permanent is true. | [optional] 
**ExpiresIn** | **int** | Seconds until the presigned uploadUrl expires (always 3600) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

