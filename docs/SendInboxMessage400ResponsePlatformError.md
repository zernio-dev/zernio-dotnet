# Zernio.Model.SendInboxMessage400ResponsePlatformError
Instagram, Facebook, or WhatsApp. Meta's diagnostic fields for the rejected send or template lookup. WhatsApp lookup errors retain only code, message, and error_data.details. Absent when the failure did not come from Meta.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int** | Meta error code | [optional] 
**Subcode** | **int** | Meta error_subcode | [optional] 
**FbtraceId** | **string** | Meta fbtrace_id, quote this in a Meta bug report | [optional] 
**Type** | **string** | Meta error type (e.g. OAuthException) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

