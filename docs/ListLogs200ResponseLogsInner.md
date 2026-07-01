# Zernio.Model.ListLogs200ResponseLogsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** | Log category (publishing, connections, webhooks, messaging) | [optional] 
**Action** | **string** | Specific action (post.published, message.sent, account.connected, etc.) | [optional] 
**UserId** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**StatusCode** | **int** |  | [optional] 
**ErrorMessage** | **string** |  | [optional] 
**ErrorCode** | **string** |  | [optional] 
**DurationMs** | **int** |  | [optional] 
**Endpoint** | **string** | The API endpoint that triggered this log | [optional] 
**RequestBody** | **string** | Request JSON (truncated to 5KB) | [optional] 
**ResponseBody** | **string** | Response JSON (truncated to 10KB) | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**Metadata** | **string** | Additional context as JSON string | [optional] 
**RequestId** | **string** | Correlation ID linking every log from one API request (api_request logs) | [optional] 
**ApiKeyId** | **string** | The API key that made the request (api_request logs) | [optional] 
**Method** | **string** | HTTP method (api_request logs) | [optional] 
**Path** | **string** | Request path (api_request logs) | [optional] 
**IpAddress** | **string** | Client IP address (api_request logs) | [optional] 
**UserAgent** | **string** | Client user-agent (api_request logs) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

