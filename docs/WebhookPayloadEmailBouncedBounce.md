# Zernio.Model.WebhookPayloadEmailBouncedBounce

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Recipient** | **string** | The address that refused the mail. | [optional] 
**Type** | **string** | &#x60;hard&#x60;: 5.x.x, the address does not take mail. &#x60;soft&#x60;: 4.x.x, a temporary refusal the sending server gave up on. &#x60;undetermined&#x60;: the report gave no status. | [optional] 
**Category** | **string** |  | [optional] 
**Status** | **string** | RFC 3463 enhanced status, such as 5.1.1. | [optional] 
**SmtpCode** | **int?** | The SMTP reply code, such as 550. Always a number. | [optional] 
**Diagnostic** | **string** | The receiving server&#39;s answer. | [optional] 
**RecommendedAction** | **string** | &#x60;remove&#x60; only for an address that does not take mail. Sender-side refusals (authentication, blocklists, spam filters) are &#x60;fix_configuration&#x60; or &#x60;review&#x60;, never &#x60;remove&#x60;. | [optional] 
**ReportingMta** | **string** |  | [optional] 
**Detection** | **string** | &#x60;dsn&#x60;: a standard delivery report with the bounced Message-ID. &#x60;ndr&#x60;: a non-standard report read from its headers and text. | [optional] 
**BounceMessageId** | **string** | Provider id of the bounce report in the mailbox. | [optional] 
**BouncedAt** | **DateTime** | When the report arrived in the mailbox. | [optional] 
**DetectedAt** | **DateTime** | When Zernio read it. Reports can arrive minutes to days after the send. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

