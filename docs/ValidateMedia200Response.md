# Zernio.Model.ValidateMedia200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Valid** | **bool** |  | [optional] 
**Url** | **string** |  | [optional] 
**Error** | **string** | Error message if valid is false | [optional] 
**Code** | **string** | Stable reason when valid is false. MEDIA_UNDECODABLE: the bytes are not a valid image, video or PDF. MEDIA_URL_UNREACHABLE: HTTP error, timeout, network failure, or a web page served instead of the file. MEDIA_URL_NOT_ALLOWED: not a public HTTP(S) URL. | [optional] 
**ContentType** | **string** | Content-Type header the server sent (may disagree with the detected format) | [optional] 
**Size** | **int?** | File size in bytes | [optional] 
**SizeFormatted** | **string** |  | [optional] 
**Type** | **string** | Detected from the file bytes | [optional] 
**Format** | **string** | Detected format (jpeg, png, webp, gif, heif, mp4, mov, webm, pdf, ...) | [optional] 
**Width** | **int** | Image width in pixels (images only) | [optional] 
**Height** | **int** | Image height in pixels (images only) | [optional] 
**Inspection** | **string** | How deeply the content was verified. decoded: every pixel decoded. header: file signature and header verified (videos, PDFs, HEIC/AVIF, images over 32 MB). | [optional] 
**PlatformLimits** | [**Dictionary&lt;string, ValidateMedia200ResponsePlatformLimitsValue&gt;**](ValidateMedia200ResponsePlatformLimitsValue.md) | Per-platform size limit comparison (only present when size and type are known) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

