# Zernio.Model.PostPlatformError
The platform's own error for this target, so you can see what the platform said (access tokens are redacted). Set when the last attempt failed with an error the platform described (currently Instagram and Facebook), and kept while an automatic retry of that failure is pending or running; cleared when the target publishes or is retried manually. errorMessage stays the human-readable summary; this block is for diagnostics and support tickets. Instagram media processing failures carry no code or subcode, only Meta's status text in message.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int** | Meta error code, when Meta sent one. | [optional] 
**Subcode** | **int** | Meta error_subcode, when Meta sent one. | [optional] 
**Message** | **string** | The platform&#39;s raw error message or media processing status text. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

