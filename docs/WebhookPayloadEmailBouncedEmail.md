# Zernio.Model.WebhookPayloadEmailBouncedEmail
The mail that bounced. `messageId`, `trackingId` and `metadata` are set when it was sent with tracking; otherwise match on `threadId`, `internetMessageId` or `subject`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MessageId** | **string** | Provider id of the sent mail. | [optional] 
**ThreadId** | **string** |  | [optional] 
**InternetMessageId** | **string** | The RFC 5322 Message-ID of the mail that bounced. | [optional] 
**TrackingId** | **string** |  | [optional] 
**Metadata** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**Subject** | **string** | From the headers the report quotes. | [optional] 
**SentAt** | **DateTime?** | From the headers the report quotes. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

